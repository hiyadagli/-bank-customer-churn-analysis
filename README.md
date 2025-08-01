# Bank Customer Churn Prediction

This project analyzes customer churn behavior for a European bank using Python. The goal is to identify which customers are at risk of leaving and uncover the key drivers behind their decisions. By leveraging data exploration, predictive modeling, and SHAP-based interpretability, we provide business-ready insights that can improve retention strategies.

---

## 📊 Problem Statement

Customer churn is a significant challenge in the banking industry. Understanding which customers are likely to leave — and why — allows banks to proactively intervene. This project answers:

- Who is most likely to churn?
- What features (age, credit score, country, etc.) drive churn risk?
- How can we interpret model predictions in a transparent, stakeholder-friendly way?

---

## 🛠️ Tools & Technologies

- **Language**: Python
- **Libraries**: `pandas`, `numpy`, `seaborn`, `matplotlib`, `scikit-learn`, `shap`
- **Modeling**: Logistic Regression, Random Forest with GridSearchCV
- **Interpretability**: SHAP (SHapley Additive Explanations)
- **Visualization**: Tableau (dashboard under development)
- **Environment**: Google Colab, GitHub

---

## 🧼 Data Cleaning Summary

- Dataset: [Bank Customer Churn Dataset (Kaggle)](https://www.kaggle.com/datasets/gauravtopre/bank-customer-churn-dataset)
- Removed unnecessary columns (e.g., `customer_id`)
- Encoded:
  - `gender` as binary
  - `country` using one-hot encoding
- No missing values in the dataset
- All features scaled using `StandardScaler`

---

## 📈 Exploratory Data Analysis (EDA)

Key trends:

- 🇩🇪 **German customers** have the highest churn (~32.5%)
- 👥 **Inactive members** churn more (~25%) than active ones (~15%)
- 👩‍🦰 **Female customers** churn more (~25%) than males (~15%)
- 📊 **Age, tenure, and credit score** all show patterns distinguishing churned vs retained customers

Visuals created with Seaborn (distribution plots, bar plots, churn rates by group).

---

## 🤖 Modeling & Performance

### Models Used:
- **Logistic Regression** (baseline)
- **Random Forest** (tuned via GridSearchCV)

### Evaluation Metrics:
| Metric         | Logistic Regression | Random Forest (Tuned) |
|----------------|---------------------|------------------------|
| Accuracy       | ~81%                | ~83%                   |
| Recall (churn) | Very low (~17%)     | 58%                    |
| ROC-AUC        | 0.76                | 0.83+                  |

---

## 🔍 Model Interpretability with SHAP

Using SHAP (TreeExplainer), we identified:

| Feature             | Effect on Churn |
|---------------------|------------------|
| `active_member`     | Inactive → more likely to churn |
| `country_Germany`   | Higher churn risk |
| `credit_score`      | Lower → more likely to churn |
| `age`               | Mid-age range (~40s) more likely |
| `estimated_salary`  | Weak/no clear effect |

SHAP summary and interaction plots allow us to understand how individual features contribute to each prediction — essential for transparency in a business context.

---

## 📌 Key Insights

- Churn is concentrated in specific groups: **inactive**, **German**, and **middle-aged** customers.
- Traditional metrics (e.g., salary) are *less predictive* than engagement-related behaviors.
- Model + SHAP offers both prediction and **explanation**, making results stakeholder-ready.

---

## 📊 Tableau Dashboard (Coming Soon)

The final project deliverable will include an interactive Tableau dashboard for stakeholder use, summarizing:

- Churn rates by country, gender, and tenure
- KPI cards and filters
- Actionable churn driver visualizations


---

## 🚀 Author

**Hiya Dagli**  
Rising sophomore, aspiring data analyst  
Connect on (https://www.linkedin.com/in/hiya-dagli-61193527b/)


