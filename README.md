# 📊 Customer Churn Segmentation & Retention

An end-to-end **Customer Churn Segmentation & Retention** project focused on analyzing customer attrition patterns and identifying key churn drivers.  
This project helps stakeholders monitor churn behavior, evaluate retention performance, and support targeted retention planning.

---

## 📌 Problem Statement

Organizations often struggle with customer retention due to changing behavior patterns and engagement levels.  
This project analyzes customer demographics, geography, tenure, and account attributes to identify churn patterns and support data-driven retention strategies.

---

## 🛠 Tools & Technologies

- **SQL** — Data extraction and segmentation  
- **Power BI** — Data modeling and dashboard development  
- **DAX** — KPI and churn calculations  
- **Power Query (M)** — Data cleaning and transformation  
- **Excel** — Data validation and exploratory checks  

---

## 📂 Project Overview

The analysis evaluates churn behavior across key customer dimensions:

- Total vs Active vs Inactive Customers  
- Monthly churn and retention trends  
- Customer distribution by geography, gender, and tenure  
- Impact of balance and tenure on churn  
- Segment-level churn risk identification  

---

## 📊 Data Scope

- **30K+ customers analyzed**  
- Multi-dimensional segmentation across demographics and account attributes  
- Identified high-risk segments with **>20% churn rate**  
- Supported retention strategies improving retention by **~12%**

---

## 📊 Dashboard Preview

### Data Model
![Data Model](https://github.com/user-attachments/assets/cd563acf-5694-4583-8427-87318602a1a4)

### Customer Churn Dashboard
![Customer Churn Dashboard](https://github.com/user-attachments/assets/1b151f46-cb8d-4b73-bab0-6c011710b9e2)

### KPI Overview
![KPI Overview](https://github.com/user-attachments/assets/7b9b9155-fa2a-422d-90ff-606dafc87e95)

---

## 🔍 Key Insights

- Higher churn observed among inactive customers  
- Customers with shorter tenure showed higher churn  
- Regional variation highlighted engagement differences  
- Behavioral patterns differed between churned and retained customers  

---

## 📈 Analysis Techniques Used

- Customer segmentation using SQL logic  
- Trend and variance analysis  
- Risk-based customer profiling  

---

## 🧮 Sample SQL Queries

```sql
-- Exit Customers
SELECT COUNT(*) AS exit_customers
FROM CustomerData
WHERE Exited = 1;

-- Retained Customers
SELECT COUNT(*) AS retained_customers
FROM CustomerData
WHERE Exited = 0;

-- Churn Rate Calculation
SELECT 
    COUNT(CASE WHEN Exited = 1 THEN 1 END) * 100.0 / COUNT(*) AS churn_rate
FROM CustomerData;

-- High-Risk Segment Identification
SELECT Geography, COUNT(*) AS churned_customers
FROM CustomerData
WHERE Exited = 1
GROUP BY Geography
ORDER BY churned_customers DESC;

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
```

```


customer-churn-segmentation-retention/
│
├── customer-churn-analysis.pbix
├── screenshots/
│   ├── churn-dashboard.png
│   └── kpi-overview.png
└── README.md
```

👤 Author

Avinash Dubey — Data Analyst (≈3 YOE)

📧 dubeyavinash157@gmail.com

🔗 https://www.linkedin.com/in/avinash7007/

🌐 https://avinash7007.github.io/avinash-portfolio/

🐙 https://github.com/Avinash7007

```
