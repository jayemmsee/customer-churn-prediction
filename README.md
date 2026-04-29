# 📉 Customer Churn Prediction: Classification & Business Insights

## 🔍 Problem Statement  
Customer churn is a key challenge for subscription-based businesses. Retaining existing customers is often more cost-effective than acquiring new ones.  
This project aims to predict which customers are likely to churn and identify the key drivers behind churn behavior.

---

## ⚙️ Tools & Technologies  
- **Python** (pandas, NumPy, matplotlib)  
- **scikit-learn** (Logistic Regression, Random Forest)  
- **Data preprocessing pipelines** (ColumnTransformer, Pipeline)  
- Jupyter Notebook  

---

## 📁 Dataset  
- Source: Telco Customer Churn Dataset (IBM/Kaggle)  
- Size: ~7,000 customers  
- Target Variable: `Churn` (1 = churn, 0 = retained)

---

## 🧠 Approach  

### 1. Data Preprocessing  
- Converted `TotalCharges` to numeric and handled missing values  
- Cleaned and encoded target variable (`Churn`)  
- Removed non-informative features (e.g., `customerID`)  
- Built preprocessing pipelines for:
  - Numeric features (imputation + scaling)  
  - Categorical features (imputation + one-hot encoding)  

---

### 2. Exploratory Insights  
- Identified class imbalance (~73% retained vs ~27% churned)  
- Observed higher churn among:
  - Short-tenure customers  
  - Month-to-month contract users  
  - Customers without support/security services  

---

### 3. Modeling  

#### 🔹 Logistic Regression (Baseline Model)  
- Provided balanced performance across metrics  
- Strong ROC-AUC (~0.84) indicating good predictive capability  

#### 🔹 Random Forest (Tuned for Recall)  
- Adjusted model to prioritize recall (catching churners)  
- Achieved ~80% recall, significantly improving detection of at-risk customers  

---

## 📊 Results  

| Model                  | Accuracy | Precision | Recall | F1 Score | ROC-AUC |
|------------------------|----------|-----------|--------|----------|---------|
| Logistic Regression    | ~0.81    | ~0.66     | ~0.56  | ~0.60    | ~0.84   |
| Random Forest (Tuned)  | ~0.72    | ~0.48     | **~0.80** | ~0.60 | ~0.82   |

---

## 🔎 Key Insights  

- **Customer tenure** is the strongest predictor of churn  
- **Month-to-month contracts** significantly increase churn risk  
- Lack of **online security** and **technical support** is associated with higher churn  
- Certain **payment methods** (e.g., electronic check) correlate with churn behavior  

---

## 💼 Business Impact  

- Early identification of at-risk customers enables proactive retention strategies  
- High-recall model helps minimize missed churn cases  
- Insights support:
  - Contract optimization strategies  
  - Service bundling (e.g., support + security)  
  - Customer lifecycle targeting (early-stage retention)  

---

## 📊 Visualizations  

*(Add plots here: confusion matrix, ROC curve, feature importance chart)*

---

## 📌 Conclusion  

This project demonstrates that model selection depends on business objectives.  
While Logistic Regression provides balanced performance, a tuned Random Forest model significantly improves recall, making it more suitable for churn detection scenarios where missing at-risk customers is costly.

---

## 🔗 Next Steps  

- Hyperparameter tuning (GridSearch / RandomizedSearch)  
- Explore advanced models (XGBoost, LightGBM)  
- Incorporate additional behavioral or usage data  
- Deploy model as an API or dashboard  

---


---

⭐️ Open to opportunities in Data Science, Analytics, and Machine Learning
