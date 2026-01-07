# Payment Risk Dashboard

## Project Overview
This dashboard monitors payment risk for a virtual financial services group offering **brokerage, asset management, and investment immigration services**.  
The dashboard allows stakeholders to quickly identify overdue or defaulted payments, high-risk clients, and trends by service type and region.

**Objective:** Provide actionable insights to help the finance team manage credit risk and prioritize follow-ups.

---

## Tools Used
- **Tableau Public** – for dashboard visualization and interactivity  
- **Python** – for dataset simulation and risk score calculation  
- **Excel** – for dataset preparation
- **ChatGPT** – for mock dataset and overall assistance

---

## Dataset
- Mock dataset simulating client payments and risk metrics.  
- Columns include:
  - `Payment_ID`, `Client_ID`, `Client_Name`  
  - `Service_Type` (Brokerage / Asset Management / Investment Immigration)  
  - `Invoice_Date`, `Due_Date`  
  - `Payment_Amount`, `Payment_Status` (Paid / Late / Default)  
  - `Risk_Score` (0–100), `Region`, `Account_Manager`  

> See `/dataset/EBC_Payment_Risk_Mock_Dataset.csv` for the full dataset.

---

## Key Metrics / KPIs
- **Total Payments** – total amount of all payments  
- **Overdue Payments** – total amount past the due date  
- **Default Rate** – percentage of payments in default  
- **Late Payment Trend** – monthly overdue payment trend  
- **Risk Score Distribution** – histogram of client risk levels  
- **Top High-Risk Clients** – table of clients with highest risk scores and overdue amounts  
- **Region / Account Manager Overview** – payment risk by geography and relationship manager

---

## Dashboard Screenshots
**Overview:**  
![Dashboard Overview](screenshots/dashboard_overview.png)

**Late Payment Trend:**  
![Late Payment Trend](screenshots/late_payment_trend.png)

**Top High-Risk Clients Table:**  
![Top Clients](screenshots/top_clients_table.png)

*(Replace the placeholders above with your actual screenshots)*

---

## Interactive Dashboard Link
Access the live interactive dashboard on **Tableau Public**:  
[Insert Tableau Public Link Here](https://public.tableau.com/)

---

## Notes / Additional Info
- Calculated Fields Used:
  - **Overdue Payment Flag:** `IF [Due_Date] < TODAY() AND [Payment_Status] <> 'Paid' THEN 1 ELSE 0 END`  
  - **Default Payment Flag:** `IF [Payment_Status] = 'Default' THEN 1 ELSE 0 END`  
  - **Risk Level:** `IF [Risk_Score] >= 80 THEN 'High' ELSEIF [Risk_Score] >= 50 THEN 'Medium' ELSE 'Low' END`  
- Interactive filters included: Service Type, Region, Account Manager, Date Range  
- Color coding used for risk levels: Green = Low, Yellow = Medium, Red = High  

---

**This project demonstrates:**  
- End-to-end dashboard development workflow  
- Payment risk analysis for financial services  
- Tableau visualization skills, KPI design, and interactive dashboards  
