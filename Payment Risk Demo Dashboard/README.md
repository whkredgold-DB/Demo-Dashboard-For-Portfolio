# Payment Risk Dashboard

## Disclaimer
This dashboard is a demonstration project created for portfolio and educational purposes only. All data, figures, entities, and insights presented herein are entirely fictional and synthetically generated.

The information does not represent actual clients, transactions, performance, or risk exposure of any organization. Any resemblance to real entities or real-world situations is purely coincidental.

This dashboard is intended solely to showcase data analytics, visualization, and storytelling capabilities and should not be used for decision-making or relied upon as a reflection of real business conditions.

## Project Overview
This dashboard monitors payment risk for a virtual financial services group offering **brokerage, asset management, and investment immigration services**.  
The dashboard allows stakeholders to quickly identify overdue or defaulted payments, high-risk clients, and trends by service type.

**Objective:** Provide actionable insights to help the finance team manage credit risk and prioritize follow-ups.

---

## Tools Used
- **Tableau Public** – for dashboard visualization and interactivity  
- **Excel** – for dataset preparation
- **ChatGPT** – for mock dataset creation and overall assistance in demo building

---

## Dataset
- Mock dataset simulating client payments and risk metrics.  
- Columns include:
  - `Payment_ID`, `Client_ID`, `Client_Name`  
  - `Service_Type` (Brokerage / Asset Management / Investment Immigration)  
  - `Invoice_Date`, `Due_Date`  
  - `Payment_Amount`, `Payment_Status` (Paid / Late / Default)  
  - `Risk_Score` (0–100), weighted rule-based calculation by ChatGPT,
    (Risk Score = 0.40 × Payment_Status_Score + 0.30 × Days_Overdue_Score + 0.20 × Amount_Score + 0.10 × Service_Type_Score)
  - `Region`, `Account_Manager`  

> See [https://github.com/whkredgold-DB/Demo-Dashboard-For-Portfolio/blob/main/Payment%20Risk%20Demo%20Dashboard/Payment_Risk_Mock_Dataset.csv] for the full dataset.

---

## Key Metrics / KPIs
- **Total Payments** – total amount of all payments  
- **Overdue Payments** – total amount past the due date  
- **Default Rate** – percentage of payments in default
- **Payments by Service Type** – stacked bar of payments made and its risk level 
- **Late Payment Trend** – monthly overdue payment trend seperated by service type
- **Risk Score Distribution** – histogram of client risk levels
- **Top High-Risk Clients** – histogram of clients with highest risk scores and overdue amounts  
- **Account Manager Overview** – payment risk and amount by manager

---

## Dashboard Screenshots
**Overview:**  
[https://github.com/whkredgold-DB/Demo-Dashboard-For-Portfolio/blob/main/Payment%20Risk%20Demo%20Dashboard/Screenshot/payment%20risk%20dashboard%20overview.png]

**Late Payment Trend:**  
[https://github.com/whkredgold-DB/Demo-Dashboard-For-Portfolio/blob/main/Payment%20Risk%20Demo%20Dashboard/Screenshot/Late%20Payment%20Trend%20by%20Service%20Type.png]

**Top High-Risk Clients:**  
[https://github.com/whkredgold-DB/Demo-Dashboard-For-Portfolio/blob/main/Payment%20Risk%20Demo%20Dashboard/Screenshot/Top%20High-Risk%20Clients.png]

---

## Interactive Dashboard Link
Access the live interactive dashboard on **Tableau Public**:  
[https://public.tableau.com/app/profile/hoong.kim.wong/viz/PaymentRiskDemoDashboard/Dashboard1?publish=yes]

---

## Notes / Additional Info
- Calculated Fields Used:
  - **Overdue Payment Flag:** `IF [Due_Date] < TODAY() AND [Payment_Status] <> 'Paid' THEN 1 ELSE 0 END`  
  - **Default Payment Flag:** `IF [Payment_Status] = 'Default' THEN 1 ELSE 0 END`  
  - **Risk Level:** `IF [Risk_Score] >= 80 THEN 'High' ELSEIF [Risk_Score] >= 50 THEN 'Medium' ELSE 'Low' END`  
- Interactive filters included: Service Type, Risk Level  
- Color coding used for risk levels: Green = Low, Yellow = Medium, Red = High  

---

**This project demonstrates:**  
- End-to-end dashboard development workflow  
- Payment risk analysis for financial services  
- Tableau visualization skills, KPI design, and interactive dashboards  
