#𝐀𝐧 𝐀𝐮𝐭𝐨𝐦𝐚𝐭𝐞𝐝 𝐄𝐦𝐚𝐢𝐥 𝐁𝐢𝐥𝐥𝐢𝐧𝐠 𝐑𝐞𝐜𝐞𝐢𝐩𝐭 𝐒𝐲𝐬𝐭𝐞𝐦

An end-to-end, serverless billing automation project that extracts billing details from uploaded files and sends real-time receipt emails  by AWS cloud and Machine Learning.

## 📦 Tech Stack

- **Amazon S3** – File storage and upload trigger
- 
- **AWS Lambda** – Serverless backend logic
-   
- **Amazon Textract** – ML-powered document data extraction
-   
- **Amazon DynamoDB** – Structured data storage
- 
- **Amazon SES** – Email service for sending receipts
-   
- **IAM** – Secure access management between services
-  
- **Python** – Lambda function logic

## 📌 Features

- Upload bill (PDF/Image) to S3
- 
- Automatically trigger Lambda
- 
- Extract key-value pairs using Amazon Textract
- 
- Store extracted data in DynamoDB
- 
- Send a confirmation email to the customer using Amazon SES
- 
- Fully serverless and automated workflow

## 🔁 Workflow

```mermaid
graph TD;
    A[File Upload to S3] --> B[Trigger Lambda Function]
    B --> C[Textract - Extract Data]
    C --> D[Process & Store in DynamoDB]
    D --> E[Send Email via SES]

##🚀 How to Deploy
Ensure you have an AWS account and permissions to use the mentioned services.

Create an S3 Bucket

Set up event trigger for object uploads

Set Up Textract Permissions

Grant Lambda access to Textract using IAM

Deploy Lambda Function

Configure environment variables for:

TABLE_NAME

SENDER_EMAIL

REGION

S3_BUCKET

Add logic to handle extraction and email sending

Create DynamoDB Table

With keys like invoice_id, customer_name, amount

Verify SES Email Address (If in Sandbox)

Verify both sender and receiver emails
