# 📊 Customer Churn Analysis & Customer Intelligence

**An end-to-end data analytics project using Python, SQL, Pandas, and SQLite to investigate customer churn, subscription performance, and revenue impact.**

---

## 📌 1. Business Problem

Customer churn occurs when customers stop using a company's products or services. For a subscription business, high churn can reduce recurring revenue and increase the cost of acquiring replacement customers.

The objective of this project is to analyse customer, subscription, and customer-support data to understand:

- **Who** is churning?
- **Why** might customers be leaving?
- **When** is churn occurring?
- **Which** customer segments require further investigation?
- **How** can the business improve retention?

## 🛠️ 2. Tech Stack

| Technology | Application |
|---|---|
| Python | Data analysis and transformation |
| Pandas | Data cleaning, grouping, and aggregation |
| NumPy | Numerical operations and feature engineering |
| SQLite | Relational data storage and extraction |
| SQL | Data retrieval and business analysis |
| Matplotlib & Seaborn | Data visualisation |
| Jupyter Notebook | Analysis and documentation |

## 📈 3. Executive KPI Dashboard

*The following figures are reported in the project reference report. They should be rechecked against the final notebook before being treated as verified results.*

| KPI | Reported Value | Business Meaning |
|---|---:|---|
| Overall Churn Rate | 28.6% | Share of customers who churned |
| Retention Rate | 71.4% | Share of customers retained |
| Monthly Contract Churn | 55.6% | Churn rate among monthly subscribers |
| Annual Contract Churn | 8.3% | Churn rate among annual subscribers |
| Average Customer Tenure | 1,451 days | Reported average customer lifetime in days |
| ARPU | ₹18.8 | Reported average revenue per user |
| Revenue Loss | 74 | Reported amount; currency and calculation basis require validation |
| CLTV Lost | 2,047 | Reported customer lifetime value lost |
| Revenue Loss Percentage | 18% | Reported revenue loss as a share of revenue |

> **Data validation note:** Confirm the currency, units, customer counts, and revenue definitions before publishing these KPIs. Revenue at risk, revenue already lost, and customer lifetime value lost are different metrics.

## 🔍 4. Key Business Insights

### Insight 1 — Overall customer churn

The reference report records a churn rate of **28.6%** and a retention rate of **71.4%**.

**Business interpretation:** Churn should be monitored alongside retention, recurring revenue, and customer lifetime value to understand the overall health of the subscription business.

**Recommended action:** Establish a consistent monthly churn report and compare results across customer segments.

### Insight 2 — Monthly versus annual contracts

| Contract Type | Reported Churn Rate |
|---|---:|
| Monthly | 55.6% |
| Annual | 8.3% |

The reported monthly-contract churn rate is approximately **6.7 times** the annual-contract churn rate.

**Business interpretation:** Contract duration may be associated with differences in customer retention. However, the figures alone do not establish that contract type causes churn.

**Recommended action:** Investigate cancellation timing, pricing, plan benefits, and customer satisfaction across both contract groups. Test suitable retention offers for eligible monthly subscribers.

### Insight 3 — Subscription plan performance

The reference report identifies the Basic subscription plan as contributing the most churn.

**Business interpretation:** A high number of churned customers does not necessarily mean the plan has the highest churn rate or the greatest financial impact.

**Recommended action:** Compare churn rate, number of churned customers, monthly recurring revenue lost, and customer lifetime value across Basic, Standard, and Premium plans.

### Insight 4 — Geographic churn patterns

The reference report identifies Karnataka as the most affected state and September 2024 as the month with the most churn.

**Business interpretation:** These are areas for investigation, not proof of a particular cause.

**Recommended action:** Review cancellation reasons, support escalations, pricing changes, and subscription activity during the affected period. Compare Karnataka with other states and September with surrounding months.

### Insight 5 — Revenue and customer value

The reference report lists revenue loss of 74, CLTV lost of 2,047, and revenue loss of 18%.

**Business interpretation:** Financial impact should be measured separately from customer count. Losing a small number of high-value customers can have a different impact from losing many low-value customers.

**Recommended action:** Prioritise customer segments using validated recurring revenue, customer lifetime value, churn status, and support history.

## 📊 5. KPIs Analysed

| KPI | Calculation |
|---|---|
| Churn Rate | Churned customers ÷ total eligible customers × 100 |
| Retention Rate | Retained customers ÷ total eligible customers × 100 |
| Churn by Plan | Churn rate calculated separately for each plan |
| Churn by State | Churn rate calculated separately for each state |
| ARPU | Revenue for the defined period ÷ eligible customers for that period |
| Average Tenure | Average time between subscription start and cancellation or the defined reporting date |
| Revenue at Risk | Defined recurring revenue associated with customers classified as high risk |
| Average Complaints per Customer | Complaint count ÷ distinct customers |
| Escalation Rate | Escalated support cases ÷ total eligible support cases × 100 |
| Churn by Contract Type | Churn rate calculated separately for each contract type |

*Metric definitions must use consistent reporting periods, denominators, and customer-level aggregation.*

## 🧹 6. Data Analysis Workflow

1. **Database connection:** Connect Python to the SQLite database.
2. **Data extraction:** Load customer, subscription, and support tables.
3. **Data cleaning:** Inspect missing values, duplicates, column names, and data types.
4. **Feature engineering:** Prepare analysis fields such as tenure, churn status, and customer segments where supported by the source data.
5. **Exploratory data analysis:** Use grouping, aggregations, and pivot tables to examine patterns.
6. **KPI calculation:** Calculate churn, retention, revenue, tenure, and support metrics.
7. **Visualisation:** Use charts to compare customer segments and identify patterns.
8. **Business recommendations:** Translate validated findings into actions that can be investigated or tested.

## 💡 7. Business Recommendations

- Investigate why monthly-contract customers have a higher reported churn rate.
- Review the Basic plan's churn rate and financial contribution before changing pricing or benefits.
- Examine the September 2024 churn peak and investigate possible contributing factors.
- Analyse support complaints, escalations, and satisfaction scores alongside churn.
- Prioritise retention outreach using validated customer risk and value measures.
- Track churn rate, retention rate, recurring revenue, and customer lifetime value consistently.

These recommendations are proposed actions based on the reported patterns; their effectiveness would need to be tested.

## 📂 8. Project Files

| File | Description |
|---|---|
| `Untitled.ipynb` | Jupyter Notebook containing the analysis |
| `customer_churn.db` | SQLite database used in the project |
| `exported_churn_data.csv` | Exported dataset, if permitted for public sharing |
| `README.md` | Project documentation and business findings |

## ▶️ 9. How to Run the Project

### Requirements

Install Python and Jupyter Notebook. Depending on the imports used in the notebook, install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

### Run the analysis

1. Clone or download this repository.
2. Open a terminal in the project directory.
3. Start Jupyter Notebook:

```bash
jupyter notebook
```

4. Open `Untitled.ipynb`.
5. Verify the database and CSV paths.
6. Run the notebook cells in order.

## ⚠️ 10. Data Limitations

- KPI figures in this README are taken from the project reference report and have not been independently recalculated here.
- Revenue figures require a confirmed currency, reporting period, and calculation definition.
- Customer-support tables may contain multiple records per customer; joins must avoid inflating customer counts.
- Correlation between support activity and churn does not prove causation.
- Risk scores should not be interpreted as confirmed future churn unless their predictive performance has been evaluated.

## 🚀 11. Future Enhancements

- Develop an interactive Power BI dashboard.
- Add reusable SQL queries for key business metrics.
- Create customer cohorts based on subscription start dates.
- Compare churn and recurring revenue across plans and contract types.
- Validate risk segmentation against actual churn outcomes.
- Add charts and verified KPI outputs to this repository.

## 👩‍💻 Author

**Kushala B R**
