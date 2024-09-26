# aws-ses-go

<h1>AWS SES Integration in GO Lang</h1>
<hr />
<p>
// Create a new session in the us-west-2 region.
// Replace us-west-2 with the AWS Region you're using for Amazon SES.
cred := credentials.NewStaticCredentials( "<ACCESS_KEY_ID>" ,"<ACCESS_KEY_SECRET>","")
</p><br/>
<p>
sess , err := session.NewSession(
        &aws.Config{
            Region: aws.String("us-east-1"), // SET YOUR ACCOUNT REGION
            STSRegionalEndpoint: endpoints.STSRegionalEndpoint(STSRegionalEndpoint),
            Credentials: cred,
        },
)
</p><br/>
<p>
// Create an SES session.
svc := ses.New(sess)
</p>
