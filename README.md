# credit-default-analysis
This end-to-end Credit Risk Suite leverages a Random Forest model and SMOTE to predict defaults. It features a 3-tier Tableau dashboard: Executive Strategy (Exposure/Risk Heatmaps), Model Intelligence (Feature Importance/What-If Simulation), and Behavioral Surveillance (Debt vs. Payment Analysis), turning raw AI into actionable bank policy.
# 🚀 AI-Powered Credit Risk Surveillance & Predictive Suite

## 📌 Project Overview
This project addresses the **$5.02B capital risk problem** by shifting from reactive reporting to proactive AI surveillance.

By leveraging a **Random Forest Classifier** and **SMOTE** to handle class imbalance, the system predicts customer defaults before they occur. The final output is a **3-tier Tableau Dashboard Suite** designed for Executive, Technical, and Operational stakeholders.

---

## 🛠️ Technical Stack

| Layer | Tools Used |
|------|------------|
| **Data Engineering** | SQL |
| **Machine Learning** | Python (Pandas, Scikit-Learn) |
| **Balancing Technique** | SMOTE (Synthetic Minority Over-sampling Technique) |
| **Predictive Model** | Random Forest Classifier |
| **Visualization** | Tableau |

---

## 🏗️ Data Pipeline & Logic

### 🔹 1. SQL Transformation
- Aggregated **30,000 raw credit records** to engineer **Repayment Lag** metrics  
- Cleaned and aliased integer variables (`1,2,3`) into readable business categories  
  - Example: *Married, Single, University*

---

### 🔹 2. Python Modeling

**Handling Class Imbalance**
- Applied **SMOTE** to balance the dataset  
- Prevented model bias against the **22.12% default minority**

**Feature Importance**
- Identified **PAY_1 (most recent payment status)** as the primary predictive driver  
- Used **Gini Importance scores**

---

## 📊 Dashboard Architecture

### 🧭 Dashboard 1: Portfolio Risk Overview (Executive)

**Goal:** High-level strategic health check

**Visuals**
- **Demographic Risk Matrix**  
  - Bivariate heatmap crossing *Education × Marriage*  
  - Identifies concentrated **risk pockets**

- **Risk Distribution by Age**  
  - Binned bar chart  
  - Reference line highlights higher volatility in younger demographics

---

### 🧠 Dashboard 2: Model Intelligence Suite (Technical)

**Goal:** AI transparency and *What-If* decision support

**Visuals**
- **Confusion Matrix**  
  - 2×2 grid validating model reliability  
  - Tracks True Positive performance

- **Policy Simulation**  
  - Dynamic histogram driven by a **Risk Sensitivity Parameter**  
  - Interactive threshold slider shows real-time Approval vs Rejection impact

---

### 🔍 Dashboard 3: Debt & Payment Surveillance (Operational)

**Goal:** Behavioral tracking for credit officers

**Visuals**
- **6-Month Payment Trend**  
  - Time-series analysis of delinquency velocity

- **Debt vs Payment Scatter**  
  - Correlation plot with **Linear Regression Trend Line**  
  - Flags **over-leveraged customers**

---

## 💼 Business Impact

✅ **Proactive Mitigation**  
Identifies behavioral red flags months before default occurs

✅ **Dynamic Strategy**  
The *What-If* simulator enables instant risk-appetite adjustments

✅ **Enhanced Accuracy**  
SMOTE-driven modeling prevents blindness to high-risk minority segments

---

## 📂 Suggested Repository Structure

```bash
credit-risk-ai/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   ├── 01_data_cleaning.ipynb
│   ├── 02_model_training.ipynb
│   └── 03_evaluation.ipynb
│
├── dashboards/
│   └── tableau_workbook.twbx
│
├── src/
│   └── utils.py
│
└── README.md
