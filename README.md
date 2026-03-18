# Project 02 – Serverless Image Processor

## Objective
Build a serverless image processing pipeline in AWS.

## Architecture
User uploads an image to Amazon S3 → S3 event triggers AWS Lambda → Lambda processes the image and stores metadata in DynamoDB → processed thumbnail is saved back to S3.

## Services Used
- Amazon S3
- AWS Lambda
- Amazon DynamoDB
- IAM
- CloudWatch
- API Gateway (optional extension)

## Project Goals
- Learn event-driven architecture
- Understand S3 event notifications
- Practice Lambda serverless workflows
- Store structured metadata in DynamoDB
- Document architecture clearly in GitHub

## Status
In progress