**Project: Text-to-Speech Converter with AWS Lambda, Polly, and API Gateway**

1. Introduction

Project Overview:
This project demonstrates how to build a serverless Text-to-Speech (TTS) converter using AWS Lambda, Polly, and API Gateway. Users can send text via an HTTP request, and the API returns an audio file of the spoken text.
Purpose and Benefits:
Provides a scalable and cost-effective solution for TTS functionality. Eliminates the need for dedicated servers—easy integration with web and mobile applications.



**Architecture Diagram:**


![image](https://github.com/user-attachments/assets/e7d5bccd-4fd7-4fe9-9c2c-5d47d92cfeb6)




2. Technologies Used

AWS Lambda:
Serverless compute service that runs the TTS conversion logic.

AWS Polly:
Service that converts text into lifelike speech.

AWS API Gateway:
Creates a REST API endpoint to trigger the Lambda function.

Programming Language:
Python 3.9 was used for this project.



3. Setup and Configuration

AWS Account Setup:
Create an AWS account or log in to an existing one.

IAM Roles and Permissions:
Create an IAM role with permissions for Lambda to access Polly. Attach the AmazonPollyFullAccess policy to the role.

Lambda Function Creation:
Create a new Lambda function, select the appropriate runtime, and attach the created IAM role.

Polly Configuration:
Polly configuration is done within the lambda function code.

API Gateway Setup:
Create a REST API in API Gateway, create a resource and a POST method, and integrate it with the Lambda function.



4. Implementation Details

Lambda Function and Python Code attached in the files


API Gateway Integration:
Configure API Gateway to pass the request body to the Lambda function.


Error Handling:
Implement try-except blocks in the Lambda function to handle potential errors.

Input/Output structure:
Input: JSON object with a text key, and optional voiceId key.

Output: mp3 audio file.



**5. Deployment**
Deploy the Lambda function and API Gateway using the AWS Management Console or AWS CLI.
Test the API endpoint with tools like Postman or Curl.
"curl -X GET "https://jnp29j54je.execute-api.us-east-1.amazonaws.com/$default/TextToSpeechConverter?text=hello,%20this%20is%20a%20tutorial%20$default!" --output output.mp3"


**7. Usage**
Provide the API endpoint URL.
Show example requests and responses in JSON format.
Provide example code snippets on how to call the API from a web browser using Javascript.


**7. Security Considerations**
Use IAM roles with the least privilege principle.
Enable API Gateway authorization if needed.


9. Troubleshooting
Common errors: IAM permission issues, Lambda timeout, API Gateway configuration errors.
Use CloudWatch Logs to debug Lambda function execution.



