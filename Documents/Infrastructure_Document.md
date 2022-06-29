# Infrastructure
Table contents:
1. AWS RDS
2. AWS Elastic Beanstalk
3. AWS S3
4. GitHub
5. CircleCI

## AWS RDS
- DB identifier: database-1
- HOST: database-1.c0ii8t6eewol.us-east-1.rds.amazonaws.com
- Engine: PostgreSQL
- Region & AZ: Region & AZ
- Publicly accessible: Yes

## AWS Elastic Beanstalk
- Application: vtphatapp-env
- Environment: vtphat-app
- Version: app-220628_235032814525
- URL: `http://vtphatapp-env.eba-cqhbnptz.us-east-1.elasticbeanstalk.com/`
- Environment properties: AWS_BUCKET, AWS_PROFILE, AWS_REGION, ENV, JWT_SECRET, PORT, POSTGRES_DB, POSTGRES_HOST, POSTGRES_PASSWORD, POSTGRES_USERNAME

## AWS S3
- Bucket: vtpbucket
- Static website hosting: Enable
- Index document: index.html
- Websiet: `http://vtpbucket.s3-website-us-east-1.amazonaws.com`
- Bucket policy:
```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "PublicReadGetObject",
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::vtpbucket/*"
        }
    ]
}
```

## GitHub
- Repo: `https://github.com/ninovuong0910/nd0067-c4-deployment-process-project-starter.git`

## CircleCI
- Project: nd0067-c4-deployment-process-project-starter
- Steps: `./CircleCI.md` 
- Environment variables: AWS_ACCESS_KEY_ID, AWS_DEFAULT_REGION, AWS_SECRET_ACCESS_KEY, AWS_BUCKET, AWS_PROFILE, AWS_REGION, ENV, JWT_SECRET, PORT, POSTGRES_DB, POSTGRES_HOST, POSTGRES_PASSWORD, POSTGRES_USERNAME