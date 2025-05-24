# PredictiveCustomerChurn
Predictive Customer Churn Analysis
# Predictive Customer Churn Analysis for a Subscription-Based SaaS Company

This project leverages machine learning to identify customers at risk of churning for a fictional SaaS business. By analyzing patterns in customer behavior and service usage, the goal is to provide actionable insights to improve customer retention strategies.

---

## Dataset

- **Source:** [Telco Customer Churn - Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
- The dataset contains demographic information, account details, and usage patterns of 7,043 customers.

---

## Business Problem

Customer churn directly impacts profitability. The objective is to build a **predictive model** that:
- Accurately identifies churn-prone customers.
- Highlights key features driving churn.
- Suggests strategic interventions based on data insights.

---

## Tools & Technologies

- **Languages:** Python
- **Libraries:** pandas, NumPy, scikit-learn, XGBoost, imbalanced-learn, SHAP, matplotlib, seaborn
- **Techniques:** 
  - SMOTE for class imbalance
  - Model evaluation (confusion matrix, precision, recall, F1-score)
  - Hyperparameter tuning with RandomizedSearchCV
  - SHAP for model explainability

---

## Exploratory Data Analysis (EDA)

Key insights:
- Customers with shorter tenures and higher monthly charges are more likely to churn.
- Subscription type (e.g., month-to-month) is strongly associated with churn.
- Electronic check payments are more common among churned users.

---

## Models Tested

| Model                | Accuracy | Recall (Churn) | F1-score (Churn) |
|---------------------|----------|----------------|------------------|
| Random Forest        | 0.78     | 0.61           | 0.59             |
| Logistic Regression  | 0.70     | 0.80           | 0.59             |
| XGBoost (Tuned)      | **0.73** | **0.75**       | **0.60**         |

> **Final Model Selected**: XGBoost with hyperparameter tuning and class weighting.

---

## Key Feature Insights (SHAP Summary)

- **High monthly charges** increase churn risk.
- **Longer contracts (1–2 years)** drastically reduce churn.
- **Low tenure** and **Fiber Optic internet** users tend to churn more.

---

## Top 10 Influential Features

- Contract duration was the most predictive feature.
- Internet service type and payment method also played major roles.

---

## Recommendations

Based on the analysis:
- **Incentivize long-term contracts** (1–2 year plans).
- **Target high-risk users** with personalized offers, especially those with:
  - Month-to-month contracts
  - High monthly charges
  - Fiber optic internet
- **Encourage automatic payment methods** (like credit card or bank transfer).

---

## Project Structure

├── data/
├── images/
│ └──PredictiveCustomerChurnPlots
├── notebook/
│ └── PredictiveCustomerChurn.ipynb
├── PredictiveCustomerChurn.html
├── README.md
└── requirements.txt


---

## 🚀 How to Run

1. Clone the repo:
git clone https://github.com/asma-00/PredictiveCustomerChurn.git
cd PredictiveCustomerChurn
2. Create a virtual environment:
python -m venv venv
source venv/bin/activate # On Windows: venv\Scripts\activate
3. Install dependencies:
pip install -r requirements.txt
4. Run the Jupyter notebook:
jupyter notebook notebooks/PredictiveCustomerChurn.ipynb

---

## 📌 Final Thoughts

This project demonstrates a complete end-to-end workflow of a data analysis / data science project:
- Problem framing
- Data preprocessing
- Model building and evaluation
- Explainability and actionable insights

Ideal for real-world applications in customer retention analytics.

---
