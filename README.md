# S3 Static Website Deployment

## Project Description
Host a static HTML/CSS/JS website on AWS S3 with optional GitHub Actions deployment.

## Features
- Host static website on S3
- Optional CloudFront CDN integration
- GitHub Actions automatic deployment

## Prerequisites
- AWS account with S3 permissions  
- Git & GitHub account  
- AWS CLI installed

## Installation Commands
Install AWS CLI:
```sudo apt install awscli -y```
```aws --version```

## Configure AWS CLI:
```aws configure```
# Enter Access Key, Secret Key, Region, Output format

## Create S3 bucket and enable website hosting:
```aws s3 mb s3://<bucket-name> --region <your-region>```
```aws s3 website s3://<bucket-name>/ --index-document index.html```

## Upload files to S3:
```aws s3 cp ./ s3://<bucket-name>/ --recursive```

## How to Run / Access
# Open in browser:
```http://<bucket-name>.s3-website-<region>.amazonaws.com```

## Improvements

- Add CloudFront for faster delivery
- Add HTTPS using ACM
- Deploy multiple environments (dev/staging/prod)
