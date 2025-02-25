# Spotify ETL Pipeline Using AWS  

## Overview  
This project implements an ETL (Extract, Transform, Load) pipeline using AWS services to process data from the Spotify API. The extracted data is stored, transformed, and loaded into Amazon Athena for analytics.  

## Architecture  
The architecture follows the ETL workflow and leverages the following AWS services:  

- **Extract:**  
  - A Python script fetches data from the Spotify API.  
  - AWS Lambda (triggered by Amazon CloudWatch) extracts data and stores it in Amazon S3 (raw_data folder).  

- **Transform:**  
  - Another AWS Lambda function processes and transforms the raw data.
  - This function is triggered automatically whenever data is ingested into raw_data folder by using s3 trigger.  
  - The transformed data is stored back in Amazon S3 (transformed_data folder).  

- **Load:**  
  - An AWS Glue Crawler infers the schema and updates the AWS Glue Data Catalog.  
  - Data is then made available for querying using Amazon Athena.  

## Tech Stack  
- **Python** (used for API interaction and Lambda functions)  
- **AWS Lambda** (serverless ETL functions)  
- **Amazon S3** (storage for raw and transformed data)  
- **Amazon CloudWatch** (triggers for Lambda)  
- **AWS Glue** (schema inference and data catalog)  
- **Amazon Athena** (querying and analytics)

## Learning Outcome - What I Learned  
Through this project, I gained hands-on experience in building a small cloud-based ETL pipeline using AWS services. I learned how to extract data from the Spotify API using Python and AWS Lambda, store and transform data in Amazon S3, and automate workflows with CloudWatch triggers. I also worked with AWS Glue to infer schema and manage metadata, enabling efficient querying in Amazon Athena. This project helped me familiarize my understanding of serverless data processing, cloud-based analytics, and error handling in ETL workflows.  
