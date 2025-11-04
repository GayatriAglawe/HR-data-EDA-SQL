📊 HR Data Analysis with SQL
🧾 Overview

This project demonstrates Exploratory Data Analysis (EDA) on HR data using MySQL.
It covers everything from database creation and data cleaning to computing employee metrics such as attrition rate, salary distribution, and demographic breakdowns.

🏗️ Project Structure
Section	Description
Database Setup	Create and select the hrdata database
Data Loading	Import employees.csv into MySQL
Data Cleaning	Convert data types, format dates, handle missing values
Feature Engineering	Add calculated fields like EmployeeCurrentStatus and Age
Analysis	Perform EDA — salary, age, department, gender, attrition, etc.
Insights	Compute key HR metrics such as attrition rate and average salary
🗂️ Files
File	Description
hrdata.sql	Main SQL script containing all database operations and queries
employees.csv	Employee dataset to be uploaded into the employees table
README.md	Project documentation
⚙️ Steps to Run the Project
1. Create the Database
CREATE DATABASE hrdata;
USE hrdata;

2. Import the Data

Upload your CSV file (employees.csv) into a table named employees.

3. Run the Analysis Script

Execute the SQL queries from hrdata.sql sequentially in MySQL Workbench or any MySQL client.

🔍 Key Analyses Included
👥 Employee Summary
SELECT COUNT(*) AS Total_Employees FROM employees;

💼 Attrition Rate
SELECT 
  (CAST(COUNT(CASE WHEN EmployeeCurrentStatus = 0 THEN 1 END) AS FLOAT) / COUNT(*)) * 100 AS Attrition_Rate
FROM employees;

💰 Salary Insights

Average Salary

Salary Distribution by Ranges

Department-wise Average Salary

🧓 Demographic Insights

Average Age

Age Distribution

Gender & Marital Status Counts

🏢 Organizational Insights

Department Count

Position Count

Manager-wise Employee Count

Termination Reasons

🧮 Example Output Metrics
Metric	Example Result
Total Employees	1,000
Current Employees	850
Attrition Rate	15%
Average Salary	$65,000
Average Age	36 years
🧰 Technologies Used

MySQL 8+

CSV Dataset

SQL (DDL, DML, Aggregate, CASE, TIMESTAMPDIFF)

📈 Possible Extensions

Connect the database to a Power BI / Tableau dashboard

Add stored procedures for reusable HR reports

Automate data refresh using a Python ETL script

🧑‍💻 Author

Your Name
📧 [your.email@example.com
]
💼 [LinkedIn / GitHub Profile]
