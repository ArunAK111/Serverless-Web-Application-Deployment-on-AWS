# 🌐 Serverless Web Application Deployment on AWS

A serverless web application built using **AWS services** to efficiently handle user requests, manage data storage, and deliver content securely and quickly. The application leverages **S3**, **API Gateway**, **Lambda**, **DynamoDB**, and **CloudFront** for a fully functional and scalable solution.

## Key Features

- **S3 Bucket**: Hosts static web content, including HTML, CSS, and JavaScript files.
- **API Gateway**: Manages REST API endpoints and triggers Lambda functions to handle GET and POST requests.
- **Lambda Functions**: Python-based functions handle CRUD operations (Create, Read, Update, Delete) on DynamoDB.
- **DynamoDB**: NoSQL database for storing and retrieving application data.
- **CloudFront**: Content Delivery Network (CDN) that serves S3 content over HTTPS, providing encryption in transit and improving application performance.

## Technologies Used

- **AWS S3**: Storage for static web content.
- **AWS API Gateway**: API management for handling HTTP requests.
- **AWS Lambda**: Serverless functions to handle backend logic.
- **AWS DynamoDB**: NoSQL database for data storage.
- **AWS CloudFront**: CDN for delivering content securely and efficiently.

## Folder Structure

├── getStudents.py # Lambda function to retrieve data from DynamoDB ├── insertStudentData.py # Lambda function to insert new data into DynamoDB ├── index.html # Static web content ├── scripts.js # Client-side logic └── README.md # Project documentation


## How It Works

1. **Static Content Hosting**: 
   - The static web content (HTML, CSS, JS) is hosted in an **S3 bucket**.
2. **API Gateway**:
   - Endpoints are created in **API Gateway** to manage user interactions, such as fetching and inserting data.
3. **Lambda Functions**:
   - Two Python-based **Lambda functions** are used: one for retrieving student data (`getStudents.py`) and another for inserting student data (`insertStudentData.py`) into **DynamoDB**.
4. **DynamoDB**:
   - The **DynamoDB** table stores student data, and the Lambda functions interact with this table to perform CRUD operations.
5. **CloudFront**:
   - **CloudFront** delivers the static content securely over HTTPS and optimizes application performance.

## Deployment Steps

1. **Create an S3 Bucket** to host your static content.
2. **Set up API Gateway** with endpoints for handling GET and POST requests.
3. **Write Lambda Functions** in Python to interact with DynamoDB.
4. **Create a DynamoDB Table** for storing the necessary data.
5. **Configure CloudFront** to serve content securely over HTTPS.
