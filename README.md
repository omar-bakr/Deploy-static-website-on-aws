# Deploying Static Website on AWS

## Prject overview
The cloud is perfect for hosting static websites that only include HTML, CSS, and JavaScript files that require no server-side processing. This project consist of two main parts the first is **Hosting a the website on S3**  and the second is **Accessing the cached website pages using CloudFront content delivery network (CDN) service.** And the reason CloudFront is used beacuse it  offers low latency and high transfer speeds during website rendering. 

## S3 bucket policy
The following policy is added allowing  objects in the bucket to be publicly readable.  

```json
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "AddPerm",
            "Effect": "Allow",
            "Principal": "*",
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::my-193735622614-bucket/*"
        }
    ]
}
```

## Website URLs
[CloudFront Domain](https://d1nbvoaqvvtkrn.cloudfront.net)

[S3 endpoint](https://my-193735622614-bucket.s3.amazonaws.com/index.html)

[Website endpoint](http://my-193735622614-bucket.s3-website-us-east-1.amazonaws.com)

## Screentshots
Screenshots of the results is included under screenshots folder .




