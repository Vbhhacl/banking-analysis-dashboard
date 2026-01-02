# Banking Risk Analytics Dashboard 🏦

## 📊 Project Overview
This Power BI project is a comprehensive **Risk Assessment & Client Portfolio Analysis** solution designed for the banking sector. The dashboard helps financial institutions minimize lending risks by analyzing client profiles, loan distribution, and deposit patterns.

By integrating data across clients, banking services, advisors, and time periods, this tool enables stakeholders to make data-driven decisions regarding credit approval, customer relationship management, and revenue optimization.

## 🎯 Business Objectives
- **Risk Mitigation:** Evaluate loan repayment likelihood by correlating income bands with credit card balances and loan types.
- **Customer Segmentation:** Categorize clients based on engagement duration and income levels to tailor financial products.
- **Revenue Tracking:** Monitor processing fees and interest-bearing assets across different banking portfolios.

## 🔑 Key Performance Indicators (KPIs)

### 1. Client Metrics
- **Total Clients:** Distinct count of active banking customers.
- **Engagement Days:** Analysis of the duration of client relationships (Customer Loyalty).
- **Income Band:** Dynamic segmentation of clients into income levels:
  - *Low (<100K)*
  - *Mid (<300K)*
  - *High (>300K)*

### 2. Loan Portfolio Analysis
- **Total Loan Exposure:** Aggregated sum of all lending products.
- **Bank Loans:** Traditional personal and housing loans.
- **Business Lending:** Capital allocated to small/medium business clients.
- **Credit Card Balance:** Outstanding revolving credit amounts.

### 3. Deposit & Liquidity
- **Total Deposits:** Combined liquidity across all account types.
- **Savings Accounts:** Interest-bearing deposit analysis.
- **Checking Accounts:** Daily transactional volume.
- **Foreign Currency:** Holdings in non-domestic currency (FX Risk).

### 4. Revenue & Fees
- **Total Fees:** Aggregate of processing and maintenance fees.
- **Processing Fees:** Calculated dynamically based on client fee structures (e.g., Standard vs. High-Net-Worth rates).

## 🛠️ Technical Implementation

### Data Modeling
- Implemented a **Star Schema** architecture connecting the central Fact table with Dimension tables: `Client`, `Banking`, `Gender`, `Advisor`, and `Date`.
- Established relationships to enable slicing data by advisor performance and demographic segments.

### Data Transformation (DAX & Power Query)
- **Data Cleaning:** Handled missing values and standardized data types for financial accuracy.
- **Engagement Logic:** Created `Engagement Timeframe` using `DATEDIFF` to calculate precise client tenure.
- **Conditional Logic:** Used DAX switches to assign `Income Band` and calculate `Processing Fees` (e.g., *Fee = Loan Amount * 0.05 for specific tiers*).

Snapshots:
home page-
<img width="1918" height="1033" alt="image" src="https://github.com/user-attachments/assets/34087b19-1e0b-4208-8ea9-a75679579030" />
loan analysis-
<img width="1918" height="1033" alt="image" src="https://github.com/user-attachments/assets/d6386987-6993-4332-aa11-1630d48d9342" />
deposit analysis-
<img width="1918" height="1038" alt="deposit analysis" src="https://github.com/user-attachments/assets/0987f6a8-be25-40ee-810e-30cc1d2f7c0f" />
summary page-
<img width="1918" height="1038" alt="deposit analysis" src="https://github.com/user-attachments/assets/ca05ae8c-e281-425a-aed8-5e4040f0a64d" />

## 🚀 How to Run
1. Download the `.pbix` file from this repository.
2. Open in **Microsoft Power BI Desktop**.
3. Interact with the filters (Year, Month, Income Band) to explore the data.

---
**Author:** Vaibhavi Halloli

