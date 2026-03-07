# 📊 Customer Churn Analysis

A comprehensive Power BI dashboard that analyzes customer churn behavior in the banking sector. This project helps stakeholders understand patterns leading to customer attrition and provides insights for improving retention strategies.

# 🧠 Problem Statement

Banking institutions face challenges in customer retention. Identifying the characteristics of customers likely to churn enables banks to proactively address issues and improve services. This project analyzes key metrics to uncover churn drivers.

# 📂 Project Overview
Tool Used: Power BI, Python , SQL Server

# Total vs. Active vs. Inactive Customers
Credit Card vs. Non-Credit Card Holders

Monthly Churn and Retention Trends

Customer Distribution by Geography and Tenure

Impact of Features like Balance, Tenure, and Services Used on Churn

# Data Model View
![Data model](https://github.com/user-attachments/assets/259ee446-dbd0-4ca6-b2f3-7de62e2f590e)


# Dashboard View 
![Summary](https://github.com/user-attachments/assets/6c7c5dab-0a7c-41db-9cfd-02a2bb766ca0)

![All kpi (2)](https://github.com/user-attachments/assets/e34cd70c-1e69-4656-a16e-5e5ab63ff777)

# 📈 Dashboard Insights
KPIs Tracked:
Total Customers

Active vs. Inactive Customers

Credit Card Holders

Churned Customers (Exited)

Retained Customers

Monthly Customer Trends

Churn by Geography, Gender, and Age

Tenure and Balance Analysis

# Visualizations:

Bar & Column Charts – Churn rate by demographics

Line Charts – Monthly churn and retention trends

Pie Charts – Service usage and credit card distribution

Slicers – Filter by Geography, Gender, and Credit Card status

Cards – Display key KPIs

# 📌 Features

Fully interactive slicers and filters

Drill-down capabilities for detailed view

Industry-standard report layout for executive presentation

Custom DAX measures for accurate KPIs

# 🛠️ Technical Stack

Power BI Desktop for data modeling and visualization

DAX (Data Analysis Expressions) for calculated columns and measures

Power Query (M language) for data cleaning and transformation


# 🧮 Sample DAX Measures

Exit Customers =
CALCULATE(
    COUNTROWS(CustomerData),
    CustomerData[Exited] = 1
)

Retained Customers =
CALCULATE(
    COUNTROWS(CustomerData),
    CustomerData[Exited] = 0
)

Churn Rate (%) =
DIVIDE([Exit Customers], [Total Customers]) * 100
