# 💳 Credit Risk Model

> **Statistical Credit Risk Modeling using Python — Default Prediction & Borrower Risk Profiling**

   

***

## 📌 Project Overview

Financial institutions face significant losses from credit card defaults. This project builds a **statistical credit risk model** that quantifies and assesses the **probability of default (PD)** for credit card clients — replicating the credit risk assessment workflows used in real banking environments.

> 💡 **Business Relevance:** This project mirrors the credit risk quantification, data-driven risk monitoring, and exception analytics workflows used by risk teams at banks such as Barclays, HDFC, and SBI. The model outputs directly support credit approval decisions and risk band classification.

The project is split into two modules:
- **`CreditRiskDataAnalysis.py`** — Exploratory Data Analysis (EDA), feature profiling, and risk pattern identification
- **`CreditRiskModel.py`** — Model building, evaluation, and default probability prediction

***

## 🎯 Key Features

| Feature | Description |
|---|---|
| **Default Prediction** | Predicts probability of credit card default for individual borrowers |
| **Risk Profiling** | Identifies high-risk borrower segments by payment behavior, bill amounts, and demographics |
| **EDA Dashboard** | Visualizes default distribution, payment patterns, and feature correlations |
| **Model Comparison** | Evaluates multiple classification models on ROC-AUC and accuracy |
| **Feature Importance** | Identifies top drivers of credit default using model-based ranking |
| **Exception Flagging** | Flags applicants above a risk threshold for manual analyst review |

***

## 📊 Dataset

**Source:** [Default of Credit Card Clients Dataset — UCI / Kaggle](https://www.kaggle.com/datasets/uciml/default-of-credit-card-clients-dataset)

- **Records:** 30,000 credit card clients (Taiwan, 2005)
- **Target variable:** `default.payment.next.month` (1 = Default, 0 = No Default)
- **Default rate:** ~22% in dataset

### Feature Summary

| Feature | Description |
|---|---|
| `LIMIT_BAL` | Credit limit amount (NT dollars) |
| `SEX` | Gender (1 = Male, 2 = Female) |
| `EDUCATION` | Education level (1=Graduate, 2=University, 3=High School) |
| `MARRIAGE` | Marital status (1=Married, 2=Single, 3=Other) |
| `AGE` | Age of the client |
| `PAY_0` to `PAY_6` | Repayment status for last 6 months (-1=Paid, 1-9=Months delayed) |
| `BILL_AMT1` to `BILL_AMT6` | Bill statement amounts for last 6 months |
| `PAY_AMT1` to `PAY_AMT6` | Amount paid in last 6 months |

***

## 🧪 Models Compared

| Model | ROC-AUC | Accuracy | Notes |
|---|---|---|---|
| Logistic Regression | Baseline | — | Interpretable, regulatory-friendly |
| Decision Tree | — | — | Rule-based, explainable |
| Random Forest | — | — | Ensemble, handles non-linearity |
| XGBoost | Best | — | Highest predictive performance |

> *Exact metrics available in notebook outputs of `CreditRiskModel.py`*

***

## 🔍 Key Business Insights

| Insight | Finding |
|---|---|
| **Top Default Driver** | Repayment status (`PAY_0`, `PAY_2`) are strongest predictors of default |
| **Payment Delay Risk** | Clients with 2+ months of payment delay show significantly elevated default probability |
| **Credit Limit Effect** | Lower credit limits (`LIMIT_BAL < 50,000`) correlate with higher default rates |
| **Demographic Patterns** | Younger clients (age 20–30) show higher default tendency |
| **Education Signal** | Less-educated borrowers show marginally higher default rates |

***

## 🗂️ Project Structure

```
credit-risk-model/
├── CreditRiskDataAnalysis.py   # EDA, visualizations, feature profiling
├── CreditRiskModel.py          # Model training, evaluation, prediction
└── README.md
```

***

## ⚙️ Tech Stack

| Category | Tools |
|---|---|
| Language | Python 3.10 |
| Data Processing | Pandas, NumPy |
| Visualization | Matplotlib, Seaborn |
| Modeling | Scikit-Learn, XGBoost |
| Dataset Source | Kaggle / UCI ML Repository |

***

## 🚀 How to Run

```bash
# 1. Clone the repository
git clone https://github.com/smeetpatel2530/credit-risk-model.git
cd credit-risk-model

# 2. Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn xgboost

# 3. Run EDA first
python CreditRiskDataAnalysis.py

# 4. Run the model
python CreditRiskModel.py
```

> **Dataset:** Download from [Kaggle](https://www.kaggle.com/datasets/uciml/default-of-credit-card-clients-dataset) and place as `UCI_Credit_Card.csv` in the project root before running.

***

## 📈 Future Improvements

- [ ] Add Streamlit dashboard for interactive risk scoring
- [ ] Implement SHAP explainability for individual predictions
- [ ] Add probability calibration (Platt scaling / isotonic regression)
- [ ] Build REST API endpoint for real-time credit scoring
- [ ] Extend to Probability of Default (PD) → Loss Given Default (LGD) → Expected Loss (EL) framework

***

## 👤 Author

**Smeet Patel**  
M.Tech in Computer Science & Engineering — Delhi Technological University (DTU)  
📧 smeetpatel2530@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/smeet-patel-22b67a193/) | [GitHub](https://github.com/smeetpatel2530) | [Portfolio](https://smeetpatel2530.github.io/CV-Upgraded/)

***


