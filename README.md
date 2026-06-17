# 📊 FinSight — Finance Analysis Dashboard

> **Real-Time Insights into Transactions, Customers & Risk**

A comprehensive financial analytics project built on a dataset of **5,000 customers** and **50,069 transactions** spanning FY 2023–2026. The project covers transaction intelligence, customer segmentation, fraud detection, risk scoring, and revenue performance analysis — visualised through an interactive Power BI dashboard and documented in a structured business report.

---

## 🗂️ Project Structure

```
finsight-finance-analysis/
│
├── data/
│   ├── customers.csv               # Customer master data (5,000 records)
│   └── finance_transactions.csv    # Transaction ledger (50,069 records)
│
├── dashboard/
│   └── FinSight_Dashboard.pbix     # Power BI dashboard file
│
├── report/
│   └── FinSight_Finance_Analysis_Report.docx  # Full business analysis report
│
├── screenshots/
│   ├── overview_analysis.png       # Overview tab screenshot
│   └── transactions_view.png       # Transactions tab screenshot
│
└── README.md
```

---

## 📁 Dataset Overview

### `customers.csv` — 5,000 Records

| Column | Description |
|---|---|
| `customer_id` | Unique customer identifier (e.g. C00001) |
| `first_name` | Customer first name |
| `second_name` | Customer last name |
| `gender` | Male / Female |
| `date_of_birth` | DOB in DD-MM-YYYY format |
| `city` | City of residence |
| `state` | State of residence |
| `occupation` | Retired / Salaried / Freelancer / Business Owner / Student / Self Employed |
| `customer_segment` | Retail / Premium / SME / Corporate / Wealth |
| `annual_income` | Annual income in INR |
| `join_date` | Platform onboarding date (DD-MM-YYYY) |

### `finance_transactions.csv` — 50,069 Records

| Column | Description |
|---|---|
| `transaction_id` | Unique transaction ID (e.g. T00000001) |
| `transaction_date` | Date of transaction (DD-MM-YYYY) |
| `account_id` | Associated account ID |
| `customer_id` | Foreign key → customers.csv |
| `transaction_type` | Investment / Transfer / Withdrawal / Deposit / Loan EMI / etc. |
| `channel` | Mobile App / UPI / Net Banking / Branch / ATM / POS / Auto Debit |
| `merchant_category` | Groceries / Rent / Salary / Healthcare / Shopping / etc. |
| `amount` | Transaction amount (INR) |
| `fee_amount` | Platform fee charged (INR) |
| `tax_amount` | Tax deducted (INR) |
| `currency` | INR |
| `transaction_status` | Success / Failed / Pending |
| `is_fraud` | Yes / No |
| `risk_score` | 0–100 risk score assigned to the transaction |
| `reference_no` | Unique reference number |

---

## 📈 Key Metrics at a Glance

| Metric | Value |
|---|---|
| Total Customers | 5,000 |
| Total Transactions | 50,069 |
| Portfolio Value | ₹45.61 Crore |
| Avg Transaction Value | ₹9,110 |
| Transaction Success Rate | **85.7%** |
| Transaction Failure Rate | **10.2%** (5,103 transactions) |
| Pending Transactions | 2,036 (4.1%) |
| Confirmed Fraud Cases | 632 (1.26%) |
| High-Risk Transactions (score ≥ 70) | 1,214 (2.4%) |
| Total Fees Collected | ₹7.27 Lakh |
| Total Tax Collected | ₹1.31 Lakh |

---

## 👥 Customer Segmentation

| Segment | Count | % Share | Avg Annual Income |
|---|---|---|---|
| Retail | 2,703 | 54.1% | ₹5.27 Lakh |
| Premium | 895 | 17.9% | ₹9.50 Lakh |
| SME | 780 | 15.6% | ₹7.15 Lakh |
| Corporate | 374 | 7.5% | ₹10.57 Lakh |
| Wealth | 248 | 5.0% | ₹15.82 Lakh |

---

## 🌍 Top States by Customer Count

| Rank | State | Customers |
|---|---|---|
| 1 | Maharashtra | 747 |
| 2 | Gujarat | 541 |
| 3 | Karnataka | 534 |
| 4 | Uttar Pradesh | 492 |
| 5 | Tamil Nadu | 482 |

---

## 🔁 Transaction Type Breakdown

| Transaction Type | Count |
|---|---|
| Loan EMI | 9,140 |
| Transfer | 8,479 |
| Card Payment | 5,329 |
| Deposit | 4,970 |
| Withdrawal | 4,279 |
| Bill Payment | 4,310 |
| Interest Credit | 4,017 |
| Fee Charge | 3,640 |
| Investment | 3,568 |
| Refund | 2,337 |

---

## 🚨 Fraud & Risk Summary

- **632 fraudulent transactions** detected out of 50,069 total
- **Retail segment** accounts for **53.2%** of all fraud (336 cases)
- **Premium segment** has the highest per-capita fraud rate at **13.5%**
- **1,214 transactions** carry a risk score ≥ 70 (high-risk threshold)
- Average risk score: **36.1** | Median: **36.0**

---

## 🗺️ Dashboard Preview

The Power BI dashboard includes two primary views:

**Overview Analysis Tab**
- KPI cards: Total Amount, Total Transactions, Avg Transaction Value, Total Fee, Total Tax
- Total Amount by Month (trend line)
- Total Amount by Transaction Status (donut chart)
- Total Amount by Customer Segment (bar chart)
- Total Amount by State (horizontal bar)
- Transaction Type Analysis table (Amount, Fees, Tax, Count)
- Total Amount by Gender (donut chart)

**Transactions Tab**
- Full transaction detail table with filters
- Filterable by Year, Dynamic Metric, Occupation, and Category

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| **Power BI Desktop** | Interactive dashboard & data visualisation |
| **Microsoft Excel / CSV** | Raw data storage and preprocessing |
| **Python (pandas)** | Exploratory data analysis & statistics |
| **Microsoft Word (.docx)** | Business analysis report generation |

---

## 📋 Business Report

A full **10–12 page business analysis report** (`FinSight_Finance_Analysis_Report.docx`) is included in the `/report` folder. It contains:

- Executive Summary with KPI snapshot
- Business Context (customer segments, geography, occupation)
- 5 Key Insights with ₹ impact quantification
- Root Cause Analysis (failure types, fraud patterns, risk distribution)
- 6 Strategic Recommendations with action plans
- Conclusion with financial impact table and KPI targets

---

## 🔍 Key Insights from Analysis

1. **Transaction Failure Crisis** — 10.2% failure rate represents ₹4.75 Cr in at-risk value. Loan EMI is the worst offender (924 failures).
2. **Fraud Concentrated in Retail** — 53.2% of all fraud hits the Retail segment; Premium has the highest per-capita fraud rate.
3. **High-Risk Exposure** — 1,214 high-risk transactions (~₹1.11 Cr) require real-time intervention before converting to fraud or chargebacks.
4. **Wealth Segment Underperforms** — Despite the highest average income (₹15.82 Lakh), Wealth customers show thin investment product penetration.
5. **Channel Data Integrity Gap** — "M@bile App" appears as a duplicate channel (765 transactions), understating true mobile adoption by ~10%.

---

## ✅ Recommendations Summary

| Priority | Action | Est. Revenue Impact |
|---|---|---|
| 🔴 Critical | Proactive Loan EMI failure prevention (balance alerts) | ₹1.5–2.0 Cr/yr |
| 🔴 Critical | Multi-layer fraud detection (ML + step-up auth) | ₹57.6 L/yr saved |
| 🟠 High | High-risk transaction real-time monitoring | ₹1.11 Cr protected |
| 🟠 High | Wealth segment product deepening (advisory + portfolio) | ₹2.0–3.5 Cr/yr |
| 🟡 Medium | Channel data cleanup + digital-first incentives | ₹0.8–1.2 Cr/yr |
| 🟡 Medium | Geographic diversification beyond top 3 states | Long-term growth |

---

## 🚀 Getting Started

### Prerequisites
- Power BI Desktop (free) — [Download here](https://powerbi.microsoft.com/desktop/)
- Python 3.8+ with `pandas` for data exploration

### Clone the repository
```bash
git clone https://github.com/your-username/finsight-finance-analysis.git
cd finsight-finance-analysis
```

### Explore the data with Python
```python
import pandas as pd

customers = pd.read_csv('data/customers.csv')
transactions = pd.read_csv('data/finance_transactions.csv')

print(customers.head())
print(transactions['transaction_status'].value_counts())
print(transactions['is_fraud'].value_counts())
```

### Open the dashboard
1. Open `dashboard/FinSight_Dashboard.pbix` in Power BI Desktop
2. If prompted, update the data source path to your local `/data` folder
3. Click **Refresh** to reload data

---

## 📌 Notes

- The `customers.csv` file contains a minor typo in the original header: `fisrt_name` (should be `first_name`). This has been retained as-is to preserve raw data integrity.
- The `channel` field in transactions contains a data quality issue: `"M@bile App"` appears as a separate value from `"Mobile App"` (765 records). Clean this before analysis if combining mobile metrics.
- All monetary values are in **Indian Rupees (INR)**.
- Date format throughout is **DD-MM-YYYY**.

---

## 📄 License

This project is for educational and portfolio demonstration purposes.  
Data is synthetic and does not represent real individuals or financial institutions.

---

## 🙋 Author

**FinSight Analytics**  
*Real-Time Insights into Transactions, Customers & Risk*

> If you find this project useful, please ⭐ star the repository!

