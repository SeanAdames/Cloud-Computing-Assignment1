# Cloud-Computing-Assignment1
S3 bucket infrastructure: Uploaded 5 files, including a basic index.html and error.html. By using an AWS policy generator I managed to provide policies to users that allow them to get object. By altering permissions S3 bucket has been set to public.
S3 bucket permissions listed below:
{
    "Version": "2012-10-17",
    "Id": "Policy1644796053506",
    "Statement": [
        {
            "Sid": "Stmt1644795714117",
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::seanadames-2022-website/*"
        },
        {
            "Sid": "2",
            "Effect": "Allow",
            "Principal": {
                "AWS": "arn:aws:iam::cloudfront:user/CloudFront Origin Access Identity EE6EPPVCEB1DX"
            },
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::seanadames-2022-website/*"
        },
        {
            "Sid": "3",
            "Effect": "Allow",
            "Principal": {
                "AWS": "arn:aws:iam::cloudfront:user/CloudFront Origin Access Identity E2WGMA0W16WJ5E"
            },
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::seanadames-2022-website/*"
        }
    ]
}


S3 arn name: arn:aws:s3:::seanadames-2022-website
S3 bucket website: http://seanadames-2022-website.s3-website-us-east-1.amazonaws.com

CloudFront infrastructure: Cloudfront for A1 was built upon my S3 bucket. Used default settings for my cloudfront.

CloudFront Distribution Name: https://d5g5jllusoquw.cloudfront.net

Known Issues: When launching index.html from my home computer, I can view the 10 second video, however whenever it is uploaded to my S3 bucket the video disappears. This may be due to an error of using a youtube video in my s3 bucket, but I am unsure.
