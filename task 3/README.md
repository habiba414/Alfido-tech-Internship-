# Task 3 – Deployment of a Serverless Function Using AWS Lambda and API Gateway

## Overview
This task demonstrates the creation and deployment of a serverless function using AWS Lambda, testing its execution within the AWS console, and exposing it publicly as an HTTP endpoint using Amazon API Gateway.

## Objective
To create and deploy a serverless function using AWS Lambda, test its execution within the AWS console, and expose it publicly as an HTTP endpoint by configuring an Amazon API Gateway trigger.

## Tools & Environment
- **Cloud Provider:** Amazon Web Services (AWS) – Lambda Service
- **Runtime:** Python 3.14
- **Trigger:** Amazon API Gateway (REST API)
- **Region:** US East (N. Virginia)
- **Code Editor:** AWS Lambda in-console code editor
- **Access Method:** Web Browser (AWS Console) and public API endpoint

## Steps Performed
1. Navigated to the AWS Lambda service via the console search
2. Opened the AWS Lambda landing page
3. Created a new function ("Author from scratch") named `MYFirstFunction`
4. Selected the runtime: Python 3.14
5. Reviewed additional function settings (durable execution, EC2 capacity provider)
6. Verified successful function creation (function overview page)
7. Wrote the function code in `lambda_function.py` to return a JSON response
8. Deployed the function code and confirmed successful update
9. Created a new test event (`TestEvent`)
10. Executed the test and verified output (Status: Succeeded)
11. Added an API Gateway trigger (new REST API)
12. Configured API security settings (Open)
13. Verified the trigger and public API endpoint URL
14. Accessed the deployed function via the API endpoint in a browser

## Result
The Lambda function was successfully created, coded, tested, and deployed. An API Gateway trigger was configured, exposing the function as a public HTTP endpoint. Accessing the endpoint returned:
```json
{"message": "Hello from Serverless!", "status": "Success"}
```

## Deliverable
Full step-by-step report with screenshots: `Task3_AWS_Lambda_Report.docx`

## Links
- **GitHub Repository:** _add your repo link here_
- **API Endpoint (demo):** `https://5kjxdxt6g0.execute-api.us-east-1.amazonaws.com/default/MYFirstFunction` (Note: this was a temporary Lambda function for the task demo — the endpoint may no longer be active)
- **Portfolio:** _add your Netlify portfolio link here_
- **LinkedIn:** _add your LinkedIn profile link here_

## Author
Habiba Shafait – Alfido Tech
