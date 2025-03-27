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

AWS Cost Estimation

Tools and Technologies

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


                    






