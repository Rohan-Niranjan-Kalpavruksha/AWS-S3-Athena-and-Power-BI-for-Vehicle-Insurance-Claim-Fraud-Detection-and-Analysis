# AWS-S3-Athena-and-Power-BI-for-Vehicle-Insurance-Claim-Fraud-Detection-and-Analysis
AWS S3, Athena, and Power BI for Vehicle Insurance Claim Fraud Detection and Analysis

📌 Project Overview
This project focuses on detecting and analyzing fraudulent vehicle insurance claims using a cloud-based data pipeline integrated with powerful BI tools. By leveraging AWS S3, Glue, Athena, and Power BI, we create an end-to-end scalable data analysis solution that highlights patterns and trends associated with insurance fraud.

🧾 Dataset  
Source: Kaggle - Vehicle Claim Fraud Detection  
Size: ~15,000 records  
Target Column: FraudFound_P (1 = Fraudulent, 0 = Legitimate)  
Key Features: AgeOfVehicle, VehiclePrice, PolicyType, Make, MaritalStatus, Sex  

☁️ Cloud Architecture & Workflow  
✅ Step 1: AWS S3  
Created a new S3 bucket  
Uploaded the dataset under /dataset/ folder  

✅ Step 2: AWS Glue  
Created IAM role with appropriate permissions  
Set up AWS Glue crawler to scan the S3 bucket and populate the Data Catalog  

✅ Step 3: AWS Athena  
Queried structured data directly from the S3 bucket  
Performed aggregations to identify fraud patterns by demographic and policy-related variables  

✅ Step 4: Power BI  
Connected Athena to Power BI via ODBC using AWS Access Keys  
Built an interactive dashboard to visualize fraud insights  

📊 Dashboard Insights  
Total Claims: 15,000  
Fraudulent Claims: 923 (~6%)  

Key Trends:  
Higher fraud in vehicles older than 6 years  
Expensive cars (> $69,000) more fraud-prone  
Policy Type: Sport-Collision has highest fraud rate (13.79%)  
Certain car makes like Mercedes, Acura, Saturn show higher fraud risk  
Demographic filters include Age, Gender, Marital Status  

📌 Visuals Used:  
KPI Cards  
Donut & Bar Charts  
Stacked Column Charts  
Filters & Slicers for drill-down  

🚀 Future Improvements  
Train predictive models (e.g., XGBoost, Logistic Regression) using AWS SageMaker  
Set up fraud alerting via AWS Lambda and SNS  
Embed dashboards in web apps using Power BI REST API or AWS QuickSight  

