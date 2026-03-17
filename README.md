# Airbnb Host Retention: AI-Driven Marketing Strategy 🏡💡
### Data & AI-Driven Marketing 

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Latest-orange.svg)](https://scikit-learn.org/)
[![Marketing Analytics](https://img.shields.io/badge/Marketing-Predictive_Analytics-green.svg)]()

## 📌 Project Overview
This project tackles a critical supply-side marketplace challenge: **Airbnb Host Churn**. Acquiring new hosts is expensive, making the retention of existing, high-quality hosts paramount to platform growth. 

This project builds a predictive churn model to identify at-risk hosts before they leave the platform. Furthermore, it translates these predictive insights into actionable, personalized marketing interventions to maximize Customer Lifetime Value (CLV).

### 🏆 Key Outcomes
* **Predictive Accuracy:** Achieved an AUC of `0.791` using `Random Forest`.
* **Interpretability:** Utilized **SHAP value analysis** to decode the "black box," providing the marketing team with transparent, host-specific churn drivers.
* **Strategic ROI:** Developed a targeted retention framework designed to be deployed via an **A/B testing** pipeline, optimizing marketing spend by focusing only on high-value, at-risk hosts.

---

## ⚙️ Methodology & Modeling Approach
The analytical pipeline was designed to balance high predictive power with business interpretability.

### 1. Data Engineering & Feature Creation
* **Behavioral Metrics:** Booking frequency, response rates, calendar update recency.
* **Performance Metrics:** Average review scores, cancellation rates.
* **Pricing & Revenue:** Average nightly rate vs. market baseline, trailing 30-day earnings.

### 2. Predictive Modeling
I established a baseline using **Logistic Regression** to understand linear relationships before training advanced ensemble models to capture non-linear behavioral patterns.
* **Models Evaluated:** Logistic Regression, Random Forest, XGBoost.
* **Handling Imbalance:** Applied SMOTE to ensure the model accurately identified the minority churn class without over-predicting.

---

## 📊 Key Drivers of Host Churn
Using SHAP values and feature importance scores, the model identified the top indicators of host flight risk:
1. **[Driver 1, e.g., Low Occupancy Rate]:** Hosts experiencing a drop in bookings over a 60-day window are highly likely to churn.
2. **[Driver 2, e.g., Declining Review Scores]:** A sudden dip in communication or cleanliness ratings heavily precedes platform abandonment.
3. **[Driver 3, e.g., Pricing Discrepancies]:** Hosts priced >15% above their local neighborhood average face lower conversion, driving frustration and churn.

---

## 🎯 AI-Driven Marketing Strategy
Data is only as good as the action it drives. Based on the model outputs, I designed a multi-tiered marketing intervention strategy:

| Risk Segment | Key Driver | Recommended Marketing Intervention |
| :--- | :--- | :--- |
| **High Risk, High Value** | Low Occupancy | **Dynamic Pricing Nudge:** Automated email offering AI-driven pricing tips to capture immediate local demand. |
| **Medium Risk** | Declining Reviews | **Educational Campaign:** Targeted content on "Superhost" communication standards and operational checklists. |
| **New Hosts (Early Churn Risk)** | Zero Initial Bookings | **Visibility Boost:** Algorithmically bump their listing for 7 days + offer a subsidized professional photography incentive. |

### Rollout & Measurement
To validate the effectiveness of these interventions, the strategy includes an **A/B testing framework**. The holdout group receives standard communications, while the treatment group receives the AI-triggered personalized interventions, allowing us to measure true incremental lift in host retention.

---

## 🛠️ Tech Stack
* **Language:** Python
* **Libraries:** `Pandas`, `NumPy`, `Scikit-Learn`, `SHAP`, `Matplotlib`, `Seaborn`
* **Techniques:** Classification, Feature Engineering, Model Interpretation, Marketing Analytics

---

## 🏁 Conclusion
By bridging the gap between machine learning and marketing strategy, this project demonstrates how predictive analytics can shift a business from reactive troubleshooting to proactive, personalized relationship management.
