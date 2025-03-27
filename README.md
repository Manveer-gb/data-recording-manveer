# data-recording-manveer
# **Substance Use Policy Implementation – UCW (Policy No. 8006)**  
### **Assignment Portfolio – Cloud-Based Analytics and Compliance Integration**
Part 1: A data-driven framework simulating policy compliance for UCW’s Substance Use Policy (Policy No. 8006) using AWS services. The objective is to use cloud technologies for governance, monitoring, and ensuring workplace safety compliance.

Part 2: An AWS-based Data Analytics Pipeline for Vancouver Sewer Infrastructure, focusing on automation, transformation, profiling, and summarization of city sewer manhole datasets.

# Table of Contents
### **Part 1: Policy Compliance with AWS**
Dataset Overview

Methodology

AWS Services Used

Data Integration 

Governance & Access Control

Conclusion

### **Part 2: Sewer Manhole Data Analytics**

Data Collection

Automation via EC2

Data Profiling and Cleaning

Metadata Management

Aggregation and Storage

 Information Protection

Governance Policy Compliance

Real-Time Monitoring and Alerts

AWS Cost Estimation

Summary and Insights

Conclusion


### **Methodology**
**Data Ingestion**

All three CSV files were uploaded to Amazon S3 for storage.

### **Amazon S3 Bucket**

The S3 buckets created for storing datasets such as worker data, program lists, and testing data.

Buckets like hr-raw-manveer, hr-copy-man, etc., were created to organize datasets for raw and processed stages.

Purpose: Demonstrates how raw CSV files were stored and segregated to support the ETL flow securely.

![image alt](https://github.com/Manveer-gb/data-recording-manveer/blob/1a00d95987f3cc0fa83781254d67dc37c8ba2e1b/Screenshot%20(175).png)

### **AWS Services Used**

| **AWS Service**	                    |     **Purpose**   |
|----------------                     |----------------|
| **Amazon S3**                       | Secure dataset storage (raw and processed)  |
|   **AWS Glue**                      |  ETL and transformation workflows   |
|  **AWS Brew**                       | DataBrew	Data profiling and cleaning    |
|   **Aws Athena**                    |   	SQL-based data querying  |
|  **AWS IAM**                        | Access control and user permissions    |
|    **AWS CloudWatch**               | 	Monitoring ETL jobs and query health |
|  **AWS QuickSight**                 | Dashboard for compliance insights     |

### **Data Integration**

**AWS Glue DataBrew**

Displays multiple DataBrew cleaning jobs executed, including:

hr-semi-job-manveer, prgm-list-cln-manveer, tstng-lst-cln-manveer

**AWS Glue DataBrew – Project Dashboard**

Shows project names and associated datasets/recipes, like:

hr-pgm-list-prjt-manveer, hr-worker-list-prj-manveer

Purpose: Demonstrates organized project tracking and recipe-based data cleaning per dataset.

![image alt](https://github.com/Manveer-gb/data-recording-manveer/blob/f2080dd3b00ddef497576482830b239e9ca7e2b3/Screenshot%20(179).png) 
![image alt](https://github.com/Manveer-gb/data-recording-manveer/blob/06cc3ca7ec1442eb3e26261eeb48fb080967cd73/Screenshot%20(180).png)

### **Amazon Athena – Query Editor for Compliance Metrics**

Athena was used to query the cleaned and joined datasets from Glue.

Data source: AwsDataCatalog using the catalog created by AWS Glue Crawlers.

Purpose: Confirms Athena is used for SQL-based analytics post-ETL to extract compliance insights (e.g., lowest salary by compliance grouping).

![image](https://github.com/Manveer-gb/data-recording-manveer/blob/89ecbb30c461c0dacfbbb8869b5aadb94c366907/Screenshot%20(181).png)

### **Governance & Access Control**

To align with UCW Policy No. 8006 and WorkSafeBC regulations:

IAM Roles: Access restricted based on department and role (e.g., HR-only access to testing data)

S3 Bucket Policies: Defined encryption and access logging

AWS KMS Encryption: Enabled at-rest and in-transit data encryption

Audit Logs: AWS CloudTrail tracked all actions on policy-related datasets

# **Conclusion** 

This project shows the use of AWS cloud tools to support UCW’s Substance Use Policy 8006. Through real data ingestion, cleaning, transformation, and policy monitoring, it shows how workforce compliance can be maintained and visualized using scalable, cloud-native solutions. Integrating policy, analytics, and governance in one platform supports proactive safety culture and enhances organizational transparency.

# **Combined Project Report: Data Analytics Platform for the City of Vancouver**
                    
### **Objective**

This combined project focuses on building a secure, scalable, and analytics-driven Data Analytics Platform (DAP) using AWS Cloud services. 

It involves two main parts:

Project 1: Migration and transformation of sewer infrastructure data using AWS tools (ETL, profiling, storage, and summarization).

Project 2: Governance, compliance, and real-time monitoring of the analytics platform using AWS security and auditing services.

The overall goal is to enable efficient, policy-compliant, and insightful data management for the City of Vancouver using modern cloud 

capabilities.

**Data Ingestion and S3 Storage**

Created Amazon S3 buckets for structured ingestion of the raw dataset sewer-manhole-facts.csv.

Uploaded raw datasets using the AWS Management Console and validated successful transfers.

S3’s scalable architecture was used to store both raw and processed data, ensuring future scalability.

Integrity tests and validations were run post-upload to confirm readiness for processing.

![image](https://github.com/Manveer-gb/data-recording-manveer/blob/409685e364837ecbeeaee44866a820d2ecf91e32/part%201%20first%20pic.png)

**Records Automation Using EC2**

Launched an Amazon EC2 instance to automate data ingestion and transformation scheduling.

Configured the EC2 server to run shell scripts and schedule uploads, minimizing manual intervention.

This improved the data flow and reduced chances of human error in dataset updates.

**Data Profiling with AWS Glue DataBrew**

Profiled datasets using AWS Glue DataBrew to assess accuracy, completeness, and quality.

Identified missing values, outliers, and column inconsistencies.

Verified readiness for transformation by inspecting schema details and detecting anomalies.

**Data Transformation and Cleaning**

Used AWS Glue Studio to apply transformation steps:

Removed extra spaces and null values

Renamed columns (e.g., geo_point → geo_point_vancouver)

Removed duplicates and standardized formats (e.g., depth, material)

Final transformed datasets were saved in Parquet format for efficient querying.

![image](https://github.com/Manveer-gb/data-recording-manveer/blob/6e3962321c0cebef26f8caf602393ee6c7b1e64b/Picture2.png)

**Metadata Cataloging and Querying with AWS Glue**

Configured AWS Glue Crawlers to automatically create metadata tables.

Datasets were cataloged for easy access in Amazon Athena, enabling SQL queries.

Metadata made it easier to join and filter datasets based on project-specific dimensions.

![image]()










