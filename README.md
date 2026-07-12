# Crime Pattern Analysis and Prediction

Interactive Power BI dashboard combined with a Python-based predictive analytics
pipeline to analyze crime trends, weapon involvement, victim demographics, and
case clearance patterns, and to predict crime severity and patterns using
machine learning — built on 1M+ public LA crime records (2020–present).

---

## 📌 Project Overview

This project has two parts:

1. **Power BI Dashboard** — transforms raw, large-scale crime data into an
   interactive visual dashboard for exploring crime trends, weapon involvement,
   victim demographics, and case clearance performance over multiple years.
2. **Python Predictive Analytics (Jupyter Notebook)** — extends the same
   dataset with a full ML pipeline to classify crime severity, predict weapon
   involvement, detect geographic crime hotspots, and mine behavioral patterns.

The objective is to transform complex, raw crime datasets into actionable
insights — both visually (BI) and predictively (ML) — to support
data-driven public safety decision-making.

---

## 🎯 Objectives

- Analyze year-wise and month-wise crime trends and identify changes over time
- Study weapon-related crimes and evaluate their contribution to overall crime
- Analyze victim demographics such as age and gender
- Identify crime-prone areas through geographical analysis
- Evaluate case clearance rates and law enforcement effectiveness
- Predict crime severity (Low/Medium/High) and weapon involvement using ML
- Detect geographic crime hotspots and behavioral patterns via clustering and
  association rule mining
- Design an interactive, user-friendly Power BI dashboard

---

## Part 1: Power BI Dashboard

### 🛠 Tools & Technologies

- **Microsoft Power BI Desktop**
- **Power Query** for data cleaning and transformation
- **DAX (Data Analysis Expressions)** for calculated measures
- **Public Crime Dataset** (Government open data source)

### 📊 Dashboard Features

- Total Crimes and Weapon Crimes KPIs
- Year-wise and month-wise crime trend analysis
- Victim age and gender distribution
- Weapon type analysis and crime contribution
- Area-wise crime hotspot visualization
- Crime trend forecasting
- Interactive slicers and drill-down functionality

---

## Part 2: Python Predictive Analytics (Jupyter Notebook)

### 📁 Dataset

- ~1,004,991 LA crime records (2020–present), 28 raw columns
- Source: Public crime dataset (Government open data)

### 🔧 Data Pipeline

- Datetime parsing (`DATE OCC`, `Date Rptd`), missing-value imputation
  (median for age, "Unknown" for categoricals)
- IQR-based outlier detection and capping across numeric features
  (Vict Age, Hour, LAT, LON)
- Feature engineering: Year, Month, Hour, Is_Weekend flag, Weapon_Used flag
- Multicollinearity check via Variance Inflation Factor (VIF)
- Dimensionality reduction using PCA

### 🤖 Models & Results

| Task | Model | Result |
|---|---|---|
| Crime severity classification (Low/Medium/High) | Decision Tree | **77% accuracy** (weighted avg) |
| Weapon-used prediction (Yes/No) | Naive Bayes (GaussianNB) | 67% accuracy |
| Crime-type prediction (exploratory) | KNN, Decision Tree | Low accuracy — exploratory baseline only |
| Crime hour / monthly count prediction (exploratory) | Linear Regression | Weak fit — exploratory baseline only |
| Crime hotspot detection | KMeans + Hierarchical Clustering | Silhouette score ≈ 0.22 |
| Behavioral pattern mining | Apriori (Association Rules) | Surfaced weekend vs. weapon-use patterns |

### 🛠 Tools & Technologies

Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, SciPy, Statsmodels
(ARIMA), mlxtend (Apriori)

---

## 📌 Key Insights

- Weapon-related crimes constitute a significant portion of total reported crimes
- Crime occurrences vary noticeably across years and locations
- Certain areas consistently appear as crime hotspots
- Adult population groups are more affected by crime
- Clearance rates vary across different crime categories
- Crime severity can be predicted from victim/location/time features with 77%
  accuracy using a Decision Tree classifier
- Weekend occurrence and weapon use show a measurable association

---

## 🚀 Future Scope

- Integration of real-time crime data sources
- Improved crime-type and count forecasting (current baselines are exploratory)
- District or neighborhood-level micro analysis
- Deploying the severity/weapon-prediction models as a lightweight API

---

## 🔗 References

- Government Open Crime Data Portals
- Microsoft Power BI Official Documentation
- Scikit-learn Documentation

---

## 👩‍💻 Author

**Shreya Nigam**
B.Tech – Computer Science and Engineering (Data Science)
Lovely Professional University

---

## 🔗 Links

- LinkedIn post (ML analysis): [View post](https://www.linkedin.com/posts/shreya275_predictiveanalytics-predictivemodeling-pythonprojects-activity-7408152780760133632-EP6O)
- LinkedIn post (Power BI dashboard): [View post](https://www.linkedin.com/posts/shreya275_powerbi-dataanalytics-dashboarddesign-activity-7407170325597179904-7_fS)
