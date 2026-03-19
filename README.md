# Project 02 – Serverless Image Processor

## Overview

This project demonstrates a serverless image processing pipeline in AWS using Amazon S3, AWS Lambda, and Amazon DynamoDB.

When a user uploads an image to S3, an event notification triggers a Lambda function. The function processes the image, stores metadata in DynamoDB, and saves a thumbnail version back to S3.

## Objective

Build a fully serverless AWS solution that:

- accepts image uploads into Amazon S3
- triggers AWS Lambda automatically using S3 event notifications
- stores image metadata in Amazon DynamoDB
- saves processed thumbnails back to Amazon S3
- demonstrates an event-driven architecture

## Architecture

```mermaid
flowchart TD

    U[User uploads image]
    S3In[Amazon S3 Upload Bucket]
    Ev[S3 Event Notification]
    L[AWS Lambda Image Processor]
    DDB[Amazon DynamoDB Metadata Table]
    S3Out[Amazon S3 Thumbnail Bucket or thumbnails folder]
    CW[Amazon CloudWatch Logs]

    U --> S3In
    S3In --> Ev
    Ev --> L
    L --> DDB
    L --> S3Out
    L --> CW

## AWS Services Used

- **Amazon S3** – stores uploaded images and processed thumbnails
- **AWS Lambda** – processes images automatically when uploads occur
- **Amazon DynamoDB** – stores image metadata
- **IAM** – manages permissions between AWS services
- **Amazon CloudWatch** – captures Lambda logs and execution details

## Learning Goals

This project is helping me practise:

- serverless architecture
- event-driven design
- S3 event notifications
- Lambda triggers and execution flow
- DynamoDB data storage
- IAM permissions design
- CloudWatch logging and troubleshooting

## Planned Build Steps

1. Create an S3 bucket for uploads
2. Create a location for processed thumbnails
3. Create a DynamoDB table for metadata
4. Create an IAM role for Lambda
5. Write and deploy the Lambda function
6. Configure S3 event notifications
7. Upload a test image
8. Confirm thumbnail creation
9. Confirm metadata is written to DynamoDB
10. Review logs in CloudWatch

## Repository Structure

```text
project-02-serverless-image-processor/
└── README.md