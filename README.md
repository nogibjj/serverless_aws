# Project3 Serverless Web Application using AWS Lambda, API Gateway, S3 Bucket

## Sentiment Analysis 
[![Python application test with Github Actions](https://github.com/nogibjj/fastapi_news/actions/workflows/main.yml/badge.svg)](https://github.com/nogibjj/fastapi_news/actions/workflows/main.yml)

## Project Architecture and Workflow

![project](https://user-images.githubusercontent.com/112578755/226981316-7e066027-0468-46d1-b2a0-2ec5d80ea915.jpg)

# Project purpose:

The project aims to build a serverless web application that is able to reuturn a sentiment report without a server, and perform Continuous Integration through Github Actions and configure Build Server to deploy changes on build (Continuous Delivery) using AWS Lambda, API Gateway and S3 bucket.

# Project process:

1. Have all the fromt-end files ready (index.html, style.css, script.js)
2. Create lambda_function and add API Gateway
<img width="886" alt="connection_lambda_APIGateway" src="https://user-images.githubusercontent.com/112578755/226983297-35607e06-355f-4247-b2fd-d61e048a95ef.png">

3. Test if 2 buckets in S3 are created successfully from the lambda function. 
4. Get the invoke URL in AWS GW and add in the getResp() in `script.js`.
5. In lambda function, create the connection to AWS Comprehend.
6. Upload the three web page files to a new S3 Bucket (in total, we should have 3 buckets)
<img width="605" alt="S3_bucket" src="https://user-images.githubusercontent.com/112578755/226985241-3f070293-6e7b-4de1-aa81-454006d1b7f5.png">
7. In the bucket, enable static web page hosting. Test the deployment! Done 🌼


# Deployed using S3 static web page

http://hostappwithemma.s3-website-us-east-1.amazonaws.com/ 

# Example Output
The input is coming from ABC news article (https://abcnews.go.com/US/shooting-reported-denver-high-school-2-adults-hospitalized/story?id=98045110)

<img width="819" alt="example_output_serverless" src="https://user-images.githubusercontent.com/112578755/226982718-c58918d6-1a35-44a6-a791-2d3aeb4d32f1.png">


# Reference

https://towardsdatascience.com/building-full-stack-serverless-nlp-applications-with-javascript-aws-c63ca365cd15
https://www.youtube.com/watch?v=n5XFPLo4Bbw

