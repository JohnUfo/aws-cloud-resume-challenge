# AWS Cloud Resume Challenge

This is my attempt at the Cloud Resume Challenge in AWS.  
What is Cloud Resume Challenge? — [The Cloud Resume Challenge](https://cloudresumechallenge.dev/) is a multi-step resume project that helps build and demonstrate skills fundamental to pursuing a career in Cloud.

## Architecture

![Architecture Diagram](/img/AWS%20Architecture%20Cloud%20Resume%20Challenge%20(1).png)

**Services Used**:

- S3
- AWS CloudFront
- Certificate Manager
- AWS Lambda
- DynamoDB
- GitHub Actions
- Terraform

## 🔥 Live Feature

When you open [muydinovu.online](https://muydinovu.online), it counts and updates the **number of viewers** in real time using AWS Lambda and DynamoDB.

Whenever the website source code (HTML, CSS, JS) is updated and pushed to GitHub, a GitHub Actions CI/CD pipeline automatically uploads the new code to the S3 bucket.  
Once the S3 upload is complete, **CloudFront invalidates its cache** so that the latest version of the website is immediately served to users without delay.
