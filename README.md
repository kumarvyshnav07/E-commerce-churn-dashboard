# 📊 E-Commerce Customer Churn Dashboard

![Power BI](https://img.shields.io/badge/Tool-PowerBI-yellow)
![Dataset](https://img.shields.io/badge/Data-Kaggle-blue)
![Status](https://img.shields.io/badge/Project-Production--Ready-brightgreen)

---

🔥 **Built an interactive Power BI dashboard that identifies high-risk customers, quantifies revenue loss due to churn, and enables data-driven retention strategies for e-commerce businesses.**

---

## ⚡ Key Highlights

* 📉 **Churn Rate Analysis** across customer segments
* 💰 **Revenue Loss Quantification** due to churn
* 🧠 **Behavioral Insights** (engagement vs retention)
* 🌍 **Geographic Risk Identification**
* 📊 Fully interactive dashboard with slicers & drill-down

---

## 🎯 Business Impact

* Identified **mid-value customers as highest revenue-risk churn segment**
* Revealed **engagement (session duration) as strongest retention driver**
* Highlighted **regional churn anomalies** impacting CX strategy
* Enabled **targeted retention campaigns → higher ROI potential**

---

## 📊 Dashboard Preview

![Executive Overview](overview.png)
![Churn Dashboard](churn.png)

---

## 🎯 Objectives

* Identify customer segments most likely to churn
* Quantify revenue loss from churned customers
* Analyze behavioral patterns affecting retention
* Provide actionable business recommendations

---

## 🛠️ Tools & Technologies

| Tool             | Purpose                   |
| ---------------- | ------------------------- |
| Power BI Desktop | Dashboard & visualization |
| Microsoft Excel  | Data cleaning             |
| DAX              | Measures & calculations   |

---

## 📂 Dataset

* **Source:** Kaggle — E-commerce Customer Behaviour Prediction
* **Records:** ~5,000 customers
* **Target:** `Churn (Yes / No)`

**Features include:**
Customer ID, Tenure, Purchase Frequency, Session Duration, Login Frequency, Region, Segment

---

## 🧠 Data Modeling

* Cleaned & transformed dataset in Excel
* Designed **star schema (fact + dimension tables)**
* Built advanced DAX measures for KPI tracking

---

## 🧮 Key DAX Measures

```dax
Churn Rate =
DIVIDE([Churned Customers], [Total Customers])

Revenue Lost =
CALCULATE(SUM(Sales[Revenue]), Sales[Churn] = "Yes")

Avg CLV (Retained) =
CALCULATE(AVERAGE(Customers[CLV]), Sales[Churn] = "No")
```

---

## 📈 Key Insights

* 🔴 Low-value customers churn **2× more**, but mid-value customers drive higher revenue loss
* 🟡 Repeat customers generate **~60% revenue** → critical retention focus
* 📉 Session duration strongly impacts churn probability
* 🌍 Certain regions show **disproportionate churn risk**

---

## 💡 Business Recommendations

* 🎯 Target mid-value customers with early churn signals
* 🎁 Launch loyalty programs for repeat purchases
* 📩 Trigger re-engagement campaigns based on inactivity
* 🌍 Investigate high-churn regions for operational issues

---

## ▶️ How to Use

1. Download dataset from Kaggle
2. Clone repository
3. Open `.pbit` file in Power BI Desktop
4. Connect dataset when prompted
5. Explore dashboard using filters & slicers

---

## 🚀 Roadmap

* [ ] ML-based churn prediction model
* [ ] Deploy to Power BI Service
* [ ] Cohort analysis & retention curves
* [ ] Real-time data integration

---

## 👨‍💻 About the Project

This project demonstrates **end-to-end data analytics skills**, including:

* Data cleaning & transformation
* Data modeling (star schema)
* Business intelligence & visualization
* Insight generation & decision support

---

## 🙌 Acknowledgements

Dataset from Kaggle.

⭐ If you found this useful, consider giving a star!
