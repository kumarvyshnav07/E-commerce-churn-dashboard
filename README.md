# 📊 E-Commerce Customer Churn Dashboard

> An interactive Power BI dashboard to analyze customer churn, engagement behavior, and revenue trends — helping e-commerce teams identify at-risk customers and drive smarter retention strategies.

![Executive Overview](overview.png)

---

## 🎯 Objectives

- Identify customer segments most likely to churn
- Quantify revenue loss attributable to churned customers
- Uncover behavioral patterns that predict retention
- Deliver actionable recommendations for marketing and CX teams

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|------|---------|
| Power BI Desktop | Dashboard development & visualization |
| Microsoft Excel | Data cleaning & preprocessing |
| DAX | Custom measures & calculated columns |

---

## 📂 Dataset

- **Source:** [Kaggle — E-commerce Customer Behaviour Prediction](https://www.kaggle.com/datasets/akshwint/ecommerce-customer-behaviour-prediction-dataset)
- **Records:** ~5,000 customer entries
- **Key Features:** Customer ID, Tenure, Purchase Frequency, Session Duration, Login Frequency, Region, Customer Segment
- **Target Variable:** `Churn` (Yes / No)

> ⚠️ The dataset is not included in this repo. Download it from Kaggle and place it in the project folder before opening the `.pbit` template.

---

## 🧠 Data Modeling

- Cleaned missing values and standardized categorical fields in Excel
- Designed a **star schema** in Power BI with a central fact table and dimension tables for customers, regions, and segments
- Built calculated columns and measures using DAX

---

## 📊 Dashboard Pages

### 1. Executive Overview
High-level KPIs: Total Revenue, Total Purchases, Churn Rate, and Revenue Lost to churn.

### 2. Churn & CLV Analysis
Segment-wise churn breakdown, Customer Lifetime Value (CLV) distribution, and churn trends over time.

### 3. Customer Insights
Engagement metrics (session duration, login frequency) and their correlation with retention.

### 4. Geographic Analysis
Region-wise churn distribution with interactive map slicers.

![Churn & CLV Dashboard](churn.png)

---

## 🧮 DAX Measures

```dax
-- Churn rate across any filter context
Churn Rate =
DIVIDE([Churned Customers], [Total Customers])

-- Revenue lost to churned customers
Revenue Lost =
CALCULATE(SUM(Sales[Revenue]), Sales[Churn] = "Yes")

-- Average CLV for retained customers
Avg CLV (Retained) =
CALCULATE(AVERAGE(Customers[CLV]), Sales[Churn] = "No")
```

---

## 📈 Key Insights

1. **Low-value customers churn at 2× the rate** of high-value segments, but represent only 18% of total revenue loss — indicating mid-tier segment churn is the bigger financial risk.
2. **Repeat customers drive ~60% of revenue**, yet account for under 30% of the customer base — a strong case for loyalty investment.
3. **Session duration is the strongest behavioral predictor of retention** — customers with >10 min avg. sessions churn at less than half the rate of low-engagement users.
4. **Region X shows disproportionately high churn** relative to its revenue contribution, suggesting a localized service or logistics issue.

---

## 💡 Business Recommendations

- **Retention campaigns** targeting mid-value customers showing early disengagement signals (declining login frequency, shorter sessions)
- **Loyalty program** with tiered rewards to convert one-time buyers into repeat customers
- **Personalized re-engagement** emails triggered by session inactivity thresholds
- **Regional deep-dive** for high-churn areas to diagnose whether the issue is delivery, pricing, or competition

---

## ▶️ How to Use

1. Download the dataset from [Kaggle](https://www.kaggle.com/datasets/akshwint/ecommerce-customer-behaviour-prediction-dataset)
2. Clone this repo and place the dataset CSV in the project folder
3. Open `E-commerce-churn-dashboard.pbit` in **Power BI Desktop**
4. When prompted, point the data source to your local CSV file
5. Explore using the filters, slicers, and drill-throughs

---

## 🚀 Roadmap

- [ ] Churn prediction model (Logistic Regression / XGBoost) in Python
- [ ] Publish to Power BI Service with scheduled refresh
- [ ] Cohort analysis and retention curves
- [ ] Real-time data pipeline via API integration

---

## 🙌 Acknowledgements

Dataset by [akshwint on Kaggle](https://www.kaggle.com/datasets/akshwint/ecommerce-customer-behaviour-prediction-dataset). If you found this project useful, a ⭐ on GitHub is appreciated!
