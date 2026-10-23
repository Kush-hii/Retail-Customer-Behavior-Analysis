# 📊 Churn Analysis & Customer Intelligence

**An end-to-end customer churn analytics project using Python, SQL, Pandas, SQLite, NumPy, Matplotlib, and Seaborn.**

## 📌 Project Overview

Customer churn analysis helps businesses understand who leaves, why they leave, and when they are most likely to leave. This project analyses an OTT subscription dataset by combining customer demographics, subscription information, and customer-support data.

### Business Questions

- **Who:** Which customers have churned or may be at risk?
- **Why:** What customer, subscription, or support patterns are associated with churn?
- **When:** During which periods is churn most pronounced?

## 🛠️ Tech Stack

- **Python:** Data analysis and feature engineering
- **Pandas & NumPy:** Data cleaning, transformation, and aggregation
- **SQLite & SQL:** Relational data storage and extraction
- **Matplotlib & Seaborn:** Data visualisation
- **Jupyter Notebook:** Interactive analysis

## 🗄️ Database Structure

The project uses three relational tables in the `customer_churn` database.

| Table | Example Fields |
|---|---|
| `db_customer` | Customer ID, name, country, state, gender, date of birth, interests, pincode |
| `db_subscription` | Customer ID, subscription start date, renewal date, subscription type, plan type, contract type, cancellation date, cancellation reason, monthly charges, CLTV, churn score |
| `db_support` | Customer ID, complaint date, escalations, CSAT score, comments |

## 📈 Key Performance Indicators (KPIs)

The following metrics and figures are reported in the project reference report.

| KPI | Reported Value |
|---|---:|
| Overall Churn Rate | 28.6% |
| Retention Rate | 71.4% |
| Monthly Contract Churn | 55.6% |
| Annual Contract Churn | 8.3% |
| Average Customer Tenure | 1,451 days |
| ARPU | ₹18.8 |
| Total Revenue | 395 |
| Revenue Loss Due to Churn | 74 |
| CLTV Lost | 2,047 |
| Revenue Loss Percentage | 18% |

**Note:** The report does not consistently specify the units and currency for all revenue figures. These values should be validated against the final dataset before being presented as verified results.

## 🔍 Key Insights

### 1. Customer Churn and Retention

The report records an overall churn rate of **28.6%** and a retention rate of **71.4%**.

**Business implication:** Customer retention is an important area for further investigation, especially among segments with higher churn.

### 2. Monthly vs. Annual Contracts

| Contract Type | Churn Rate |
|---|---:|
| Monthly | 55.6% |
| Annual | 8.3% |

The report identifies a substantial difference between monthly and annual contract churn. The reported monthly churn rate is approximately 6.7 times the annual rate.

**Business implication:** Investigate differences in commitment periods, pricing, subscription benefits, and customer experience. The comparison alone does not establish causation.

### 3. Subscription Plan

The report identifies the Basic subscription plan as contributing the most churn.

**Business implication:** Compare the number of churned customers, the churn rate, and the revenue impact across Basic, Standard, and Premium plans before deciding which segment needs the most attention.

### 4. Geographic and Monthly Patterns

The report identifies **Karnataka** as the most affected state and **September 2024** as the month with the most churn.

**Business implication:** Investigate possible pricing changes, technical issues, customer complaints, and cancellation reasons during the affected period.

### 5. Revenue and Customer Lifetime Value

The report lists revenue loss of 74, CLTV lost of 2,047, and revenue loss of 18%.

**Business implication:** Evaluate churn using both customer counts and financial impact. Confirm the units and calculation methods before interpreting these amounts as actual losses.

## 🧮 KPI Calculation Methods

| Metric | Formula |
|---|---|
| Churn Rate | Churned customers / Total customers × 100 |
| Retention Rate | 100% − Churn Rate |
| Churn by Plan | Calculate churn rate grouped by plan type |
| Churn by State | Calculate churn rate grouped by country and state |
| ARPU | Revenue for the defined period / Eligible active customers |
| Average Customer Tenure | Average time between subscription start and cancellation or the reporting date |
| Revenue at Risk | Monthly charges associated with customers whose churn score exceeds 70 |
| Escalation Rate | Escalated support cases / Total eligible support cases × 100 |
| Average Complaints per Customer | Total complaints / Distinct customers |
| Escalation and Churn Comparison | Compare churn rates for customers with and without escalations |

*Calculation definitions should be aligned with the available columns and the reporting period used in the notebook.*

## 💡 Recommended Business Actions

1. **Investigate Karnataka:** Review customer complaints, technical issues, pricing changes, and cancellation reasons.
2. **Review the Basic plan:** Check whether changes to subscription pricing or benefits could be associated with the September 2024 churn pattern.
3. **Study competitor switching:** Investigate recorded cancellation reasons and customer feedback.
4. **Prioritise at-risk customers:** Review medium- and high-risk customers, their lifetime value, and their support history.
5. **Improve customer support:** Examine complaint trends, escalations, and customer satisfaction alongside churn.
6. **Monitor financial impact:** Track recurring revenue, churn, retention, and customer lifetime value consistently.

These are recommended investigations based on the report's findings, not confirmed explanations for churn.

## 🔄 Project Workflow

1. Connect Python to SQLite.
2. Extract customer, subscription, and support data.
3. Clean data and handle missing values.
4. Perform feature engineering and create analytical fields.
5. Conduct exploratory data analysis using aggregations, grouping, and pivot tables.
6. Calculate churn, retention, tenure, revenue, and support KPIs.
7. Create visualisations using Matplotlib and Seaborn.
8. Summarise findings and develop business recommendations.

## 🚀 Portfolio Project Summary

### Churn & Revenue Impact

Analysed an OTT subscription dataset by integrating customer and subscription information to investigate churn patterns, contract performance, and revenue impact.

The reference report identifies a 28.6% overall churn rate and a difference between monthly-contract churn (55.6%) and annual-contract churn (8.3%).

### Risk Scoring & Segmentation

Examined customer churn-risk scores, subscription characteristics, tenure, and support-related information to identify customer groups for further investigation and potential retention outreach.

### Support Intelligence & Cancellation Analysis

The reference report also describes support-escalation and cancellation analysis as ongoing work. Treat these findings as work in progress unless the analysis has been completed and verified in the notebook.

## 📂 Project Files

- `customer_churn_data_raw.xlsx` — Original Excel dataset.
- `exported_churn_data.csv` — Exported customer churn data.
- `customer_churn.db` — SQLite database.
- `Untitled.ipynb` — Jupyter Notebook containing the analysis.
- `README.md` — Project documentation, KPIs, and business findings.

## ▶️ How to Run

Install the libraries required by the notebook:

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

1. Clone or download the repository.
2. Open a terminal in the project folder.
3. Run `jupyter notebook`.
4. Open `Untitled.ipynb`.
5. Check the database and dataset paths.
6. Execute the notebook cells in order.

## ⚠️ Data Limitations

- KPI values are taken from the project reference report and require validation against the final notebook.
- Revenue figures require confirmed units, currency, and calculation definitions.
- Multiple support records for one customer can inflate counts if joins are not handled correctly.
- Associations between support activity and churn do not prove causation.
- Churn-risk scores should not be described as a validated predictive model unless their predictive performance has been evaluated.

## 👩‍💻 Author

**Kushala B R**

*For educational and portfolio purposes. Ensure that all publicly shared datasets are authorised for redistribution and do not expose private or confidential customer information.*
