* Everything in region: eu-central-1

# Create Service

* Create Stack: website-ide
* Create User "website-ide-uploader" with Programmatic Access and Inline Policy "policy"
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "VisualEditor0",
            "Effect": "Allow",
            "Action": [
                "s3:PutObject",
                "s3:DeleteObject"
            ],
            "Resource": "arn:aws:s3:::cube-codes-website-ide-storage/*"
        }
    ]
}

* Create CNAME entry in DNS from DomainName to CloudFront Hostname