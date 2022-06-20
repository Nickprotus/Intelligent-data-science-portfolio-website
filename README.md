# Intelligent data science portfolio website

#### EXPLORE Data Science Academy Cloud Computing Predict
## Overview

In this project, nivolves using Python and AWS to create an intelligent data science portfolio website. At a high-level, the website was hosted in a serverless manner on AWS; showcasing my amazing data science, machine learning and AI projects.

Below follows a brief description of each module in the system:

>- [x] **[GitHub Template Repo:](https://github.com/)** This dedicated EXPLORE template repo which houses all the content and instructions for a student to complete the Predict. 
>
>- [x] **[AWS Lambda:](https://aws.amazon.com/lambda/)** A serverless compute instance responsible for multiple processing steps:
>      - Stores the enquiry details within an AWS DynamoDB instance for later retrieval.
>      - Forwards the enquiry contents to AWS Comprehend to help formulate an intelligent response to the site visitor.
>      - Provides logic to formulate an intelligent response based on AWS Comprehend output.
>      - Upon successful completion of these tasks, invokes AWS SES to send emails to the website enquirer and an automated marking email address hosted by EDSA.
>      
>- [x] **[AWS Amplify:](https://aws.amazon.com/amplify/)** Responsible for serving the static web content hosted in GitHub which becomes the basis of the student web page.
>
>- [x] **[Amazon DynamoDB:](https://aws.amazon.com/dynamodb/)** A NoSQL database responsible for storing enquiry details from individuals visiting the student webpage.
>
>- [x] **[Anazon SES:](https://aws.amazon.com/ses/)** A code-driven email service responsible for returning an intelligent response to webpage visitors based upon their enquiries.
>
>- [x] **[AWS API Gateway:](https://aws.amazon.com/api-gateway/)** AWS service responsible for receiving enquiry details via an API call from the student webpage, and for passing these on to the internal lambda function.
>
>- [x] **[AWS Comprehend:](https://aws.amazon.com/comprehend/)** An intelligent NLP  service capable of characterising sentiment and extracting key-phrases from the ingested text. Used to detect topics within the received webpage enquiries.

## Predict Instructions

The project involves distinct steps which follow on from one another sequentially.

Brief description of each step in the 9-step predict process:

  [Step 1:](#1_section_id) Creating a **private** fork of the repo (EDSA Cloud-Computing template repo) that stores all of the code needed to host the static website. 
    
  [Step 2:](#2_section_id) This is all about customising the static website to suit your needs. You will use the provided bootstrap template and general guides to modify the look and contents of the website to fit your preferences. 
    
  [Step 3:](#3_section_id) Using AWS Amplify to serve the modified website. We provide the initial steps to begin this process, and then leave the remainder of the task as an exercise for you to understand and complete. 
  
  [Step 4:](#4_section_id) This step involves the creation of an AWS DynamoDB NoSQL database. This database will be used to store website data as and when visitors send an enquiry. 
    
  [Step 5:](#5_section_id) Creation of an IAM role that will give the AWS Lambda function (created in step 6) the required permissions to interact with AWS Comprehend, AWS SES, AWS DynamoDB and AWS API Gateway.
    
  [Step 6:](#6_section_id) This tep involves setting up the AWS Lambda function, a Numpy ARN layer, and an AWS API Gateway trigger:
    
   - **The AWS Lambda Function** will be used to:
        - Write data to Amazon DynamoDB;
        - Generate intelligent email responses with Amazon Comprehend, and
        - Send emails with Amazon SES.

   - **Numpy ARN:**
        - AWS Lambda runs Python on a Linux operating system. This means if you want to use popular libraries such as Numpy in your lambda function, you need to configure your Linux environment accordingly. You can do this by adding layers to your lambda function. In the case of Numpy, you will be adding the relevant layer to your Linux environment.

   - **The AWS API Gateway trigger** configures a publicly accessible HTTP API which listens for POST requests from the webpage. When a request is received, its content is parsed and used to invoke the connected lambda function.   
    
  [Step 7:](#7_section_id) Configuring the Lambda function created previously to write incoming data from the website to the DynamoDB database created in step four.
    
  [Step 8:](#8_section_id) Configuration of the AWS SES service so that your pipeline can send emails automatically with the help of a Lambda function.
    
  [Step 9:](#9_section_id) The final step involves completing the NLP portion with the use of AWS Comprehend and by defining additional program logic. At a high level, AWS Comprehend will be used to extract sentiment and key phrases from a message sent from your static website. Using programming logic, also involves defining several helper methods and functions which will enable the population of an automated response if the extracted key phrases and sentiment align to specific operating conditions. 
