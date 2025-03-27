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

Data Integration & Transformation

Policy Monitoring Metrics

Governance & Access Control

Cost Estimation

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

**ETL via AWS Glue**

Datasets were cleaned, standardized, and merged using AWS Glue Studio. 

**Key transformations included:**

Merging names and roles for ID matching

Cleaning inconsistencies in department names

Filtering only Active employees for compliance analysis

**Data Profiling**

Using AWS Glue DataBrew, all datasets were profiled for:

Missing values (e.g., test results or job titles)

Duplicate records

Gender distribution across departments








