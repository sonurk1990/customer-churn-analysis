# 📊 Customer Churn Analysis & Prediction
### Saiket Systems — Data Science Internship Project
**Intern:** Sonu Kumar | **Duration:** March 2026 – April 2026 | **Mode:** Remote

---

## 🎯 Project Overview

Customer churn refers to when a customer stops using a company's service. This project builds a complete **end-to-end Machine Learning pipeline** to predict which telecom customers are likely to churn, using the **Telco Customer Churn Dataset**.

The goal is to help businesses proactively identify at-risk customers and take retention actions before they leave.

---

## 📁 Project Structure

```
Customer-Churn-Analysis/
│
├── 📂 Dataset/
│   └── Telco_Customer_Churn_Dataset.csv       # Raw dataset (7,043 records, 21 features)
│
├── 📂 Notebook/
│   └── Saiket_Churn_Analysis.ipynb            # Complete Jupyter Notebook (6 Tasks)
│
├── 📂 Output_Screenshots/
│   ├── churn_distribution.png                 # Churn count chart
│   ├── contract_vs_churn.png                  # Contract type vs churn
│   ├── feature_importance.png                 # Random Forest feature importance
│   ├── confusion_matrix.png                   # Confusion matrix (RF)
│   ├── model_comparison.png                   # Model performance comparison
│   └── revenue_impact.png                     # Revenue impact chart
│
├── 📂 Presentation/
│   └── Customer_Churn_Sonu_Kumar_FINAL.pptx   # 11-slide professional PPT
│
├── 📂 Report/
│   └── Customer_Churn_Report_SonuKumar.docx   # Detailed project report
│
├── 📂 Readme/
│   └── README.md                              # This file
│
└── requirements.txt                           # Python dependencies
```

---

## 📋 Tasks Covered (6 Tasks)

| Task | Description | Status |
|------|-------------|--------|
| ✅ Task 1 | Data Loading & Preprocessing | Complete |
| ✅ Task 2 | Exploratory Data Analysis (EDA) | Complete |
| ✅ Task 3 | Customer Segmentation | Complete |
| ✅ Task 4 | Churn Prediction Model | Complete |
| ✅ Task 5 | Model Evaluation | Complete |
| ✅ Task 6 | Business Recommendations | Complete |

---

## 📊 Dataset Information

- **Source:** [Telco Customer Churn — Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
- **Records:** 7,043 customers
- **Features:** 21 columns
- **Target Variable:** `Churn` (Yes / No)
- **Churn Rate:** ~26.5%

### Key Features Used:
| Feature | Type | Description |
|---------|------|-------------|
| tenure | Numeric | Months with the company |
| MonthlyCharges | Numeric | Monthly bill amount |
| TotalCharges | Numeric | Total amount charged |
| Contract | Categorical | Month-to-month / 1yr / 2yr |
| InternetService | Categorical | DSL / Fiber optic / None |
| PaymentMethod | Categorical | Electronic check / others |
| Churn | Binary | Target: Yes / No |

---

## 🔧 Data Preprocessing

- Fixed `TotalCharges` column (blank strings → NaN → float)
- Dropped 11 null rows
- Label Encoded binary categorical columns (Yes/No → 0/1)
- One-Hot Encoded multi-class features (Contract, PaymentMethod, InternetService)
- Applied **StandardScaler** to numeric features
- **80/20 Train-Test Split** | random_state=42

---

## 📈 Exploratory Data Analysis (EDA)

Key patterns discovered:
- **Month-to-Month contracts** → 42% churn rate (vs 3% for 2-year)
- **Electronic Check** payment users → highest churn
- **New customers (tenure < 12 months)** → highest at-risk group
- **High MonthlyCharges (>$70)** → significantly increased churn
- **No Tech Support / Online Security** → 2x churn risk

---

## 🤖 Machine Learning Models

Three models were trained and compared:

| Model | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|-------|----------|-----------|--------|----------|---------|
| **Logistic Regression** 🏆 | **79.91%** | 64.26% | 54.81% | 59.16% | **84.03%** |
| Decision Tree | 78.42% | 60.36% | 54.55% | 57.30% | 82.46% |
| Random Forest | 79.21% | 63.73% | 50.27% | 56.20% | 82.25% |

> **Best Model:** Logistic Regression — highest accuracy (79.91%) and ROC-AUC (84.03%)

---

## 🔍 Feature Importance (Random Forest)

| Rank | Feature | Importance Score |
|------|---------|-----------------|
| #1 | TotalCharges | 0.187 |
| #2 | MonthlyCharges | 0.179 |
| #3 | tenure | 0.154 |
| #4 | Contract | 0.080 |
| #5 | PaymentMethod | 0.050 |

---

## 💰 Revenue Impact

| Metric | Value |
|--------|-------|
| Churned Customers | 1,869 |
| Monthly Revenue Lost | $139,130.85 |
| Annual Revenue Lost | $1,669,570.20 |
| Avg Customer Lifetime Value | $2,552.88 |
| Total Revenue at Risk | $4,771,337.38 |

---

## 💡 Business Recommendations

1. **Target Month-to-Month customers** — offer discounts to switch to annual contracts
2. **First-year onboarding program** — assign dedicated support to new customers
3. **Price sensitivity intervention** — contact high-bill customers proactively
4. **Bundle add-on services** — free trial of Tech Support / Online Security
5. **Loyalty rewards** — bill credits for long-tenure customers
6. **Deploy model in production** — monthly churn prediction alerts for sales team

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Python 3.x | Core language |
| Pandas | Data manipulation |
| NumPy | Numerical operations |
| Matplotlib | Visualization |
| Seaborn | Statistical plots |
| Scikit-learn | ML models & evaluation |
| Jupyter / Google Colab | Development environment |
| GitHub | Version control |

---

## 🚀 How to Run

```bash
# 1. Clone the repository
git clone https://github.com/yourusername/Customer-Churn-Analysis.git
cd Customer-Churn-Analysis

# 2. Install dependencies
pip install -r requirements.txt

# 3. Open the notebook
jupyter notebook Notebook/Saiket_Churn_Analysis.ipynb
```

---

## 📦 Requirements

```
pandas
numpy
matplotlib
seaborn
scikit-learn
jupyter
```

---

## 🏢 Internship Details

- **Company:** Saiket Systems
- **Website:** [www.saiket.in](https://www.saiket.in)
- **LinkedIn:** [Saiket Systems](https://www.linkedin.com/company/saiket-systems/)
- **Role:** Data Science Intern
- **Duration:** 17/03/2026 – 17/04/2026

---

## 👤 Author

**Sonu Kumar**
Data Science Intern | Saiket Systems

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue)](https://linkedin.com)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black)](https://github.com)

---

*#SaiketSystems #SaiketTech #SaiketInternship #DataScience #MachineLearning #Python*
