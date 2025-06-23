# 📊 From Upload to Inbox — Billing Automation with AWS

This project is a fully automated, serverless billing system that extracts data from uploaded PDFs/images and sends real-time billing receipt emails — powered by AWS Cloud and Machine Learning.

---

## 🚀 Tech Stack

- **Amazon S3** – For storing uploaded bills (PDFs/Images)
- **AWS Lambda** – Core logic for processing and automation
- **Amazon Textract** – ML model for extracting key-value data from documents
- **Amazon DynamoDB** – Stores structured billing data
- **Amazon SES** – Sends email receipts
- **IAM** – Secure roles and access control between services
- **Python** – Used for Lambda functions

---

## 💡 Features

- Upload a bill (PDF or image) to S3
- Automatically trigger a Lambda function
- Extract billing details using Amazon Textract
- Save the structured data to DynamoDB
- Email the receipt to the customer using SES
- 100% Serverless and real-time automation

---

## 🔁 Workflow Overview

```mermaid
graph TD;
    A[📤 File Uploaded to S3] --> B[⚙️ Lambda Triggered]
    B --> C[🧠 Amazon Textract Extracts Data]
    C --> D[💾 Data Stored in DynamoDB]
    D --> E[✉️ Email Sent via Amazon SES]
