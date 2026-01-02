# Banking Analysis Dashboard 🏦

## 📊 Project Overview
This banking analytics solution provides a comprehensive view of **Client Profiles, Loan Portfolios, and Deposit Patterns**. It helps financial institutions analyze client behavior, income distribution, and engagement metrics to support strategic decision-making in customer management and operational growth.

The dashboard integrates data across Clients, Banking Services, Advisors, and Time Periods to provide a holistic view of the bank's performance.

## 🎯 Key Performance Indicators (KPIs)

### 1. Client Metrics
- **Total Clients:** Distinct count of active banking clients.
- **Engagement Days:** Duration of client relationships with the bank (Customer Loyalty).
- **Income Band:** Categorized client income levels (Low, Mid, High).

### 2. Loan Portfolio
- **Total Loan:** Combined value of bank loans, business lending, and credit card balances.
- **Bank Loan:** Sum of traditional personal/housing loans.
- **Business Lending:** Loans allocated to small businesses.
- **Credit Cards Balance:** Outstanding credit card debt.

### 3. Deposit Analysis
- **Total Deposit:** Combined liquidity across all account types.
- **Bank Deposit:** Core banking deposits.
- **Savings Account:** Interest-bearing deposit accounts.
- **Checking Accounts:** Daily transactional accounts.
- **Foreign Currency Account:** Holdings in non-domestic currency.

### 4. Revenue Metrics
- **Total Fees:** Processing and maintenance fees calculated as a percentage of loans.
- **Processing Fees:** Variable fees generated based on client fee structures.

## 🔧 Data Transformation & Calculations
This project involves data cleaning, relationship modeling, and custom DAX calculations to derive actionable insights:

- **Engagement Timeframe:** Categorization of client relationship duration.
- **Engagement Days:** Exact count of days since the client joined (calculated using `DATEDIFF`).
- **Income Band:** Dynamic grouping of clients into income tiers:
  - *<100K:* Low
  - *<300K:* Mid
  - *Else:* High
- **Processing Fees:** Dynamic fee calculation based on client service level (e.g., High tier = 0.05).

## 🛠️ Tools Used
- **Power BI** (Dashboarding & Visualization)
- **DAX** (Data Analysis Expressions for custom metrics)
- **Power Query** (Data Cleaning & Transformation)

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

