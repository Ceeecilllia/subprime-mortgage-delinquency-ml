# subprime-mortgage-delinquency-ml

This project forecasts short-term delinquency risks across 300+ subprime mortgage pools.  
It integrates feature engineering, supervised classification models, and model interpretability to identify high-risk pools using historical performance data.

---

## 🏦 Background

Subprime loans often exhibit volatility in delinquency and default risk.  
By summarizing pool-level characteristics (e.g. FICO, LTV, prior delinquency), we build a classification model to flag pools with elevated risk.

---

## 🛠️ Workflow Summary

- 📊 **Data Aggregation:**  
  Converted loan-level data into pool-level summary statistics for 300+ mortgage pools.

- 🧪 **Feature Engineering:**  
  Created 12+ features such as:
  - `mean_fico`, `std_fico`, `ltv_median`, `volatility_delinquency`
  - `loan_count`, `prior_delinquency_rate`

- 🤖 **Modeling:**  
  - Models: Logistic Regression, Random Forest, XGBoost
  - Tuning: GridSearchCV + 5-fold cross-validation
  - Evaluation: AUC, Accuracy, Precision, Confusion Matrix

- 🔍 **Interpretability with SHAP:**  
  Used `SHAP` to identify most influential features (e.g. delinquency volatility, pool size)

---

## 📌 Key Findings

- Best model: **XGBoost** with AUC ≈ 0.87  
- **Top features:** delinquency volatility, pool size, credit quality dispersion  
- ~30 high-risk pools were flagged with >3× average short-term delinquency  
- SHAP summary revealed clear non-linear interactions

---

## 📁 Files

| File | Description |
|------|-------------|
| `summary_300_pools.csv` | Cleaned pool-level input data |
| `Project2_Group8_code.html` | Full modeling pipeline (EDA, model, SHAP) |
| `plots/` | Visualizations (SHAP, AUC, confusion matrix) |

---

## 🚧 Future Work

- Build a **Streamlit interface** for interactive pool risk querying (WIP)
- Extend to time-series risk forecast (multi-month horizons)

---

## 🧪 Note

> 🧩 This is a capstone-level course project completed at Columbia University.  
> 🧠 Focuses on real-world risk modeling in structured finance with model explainability.

---

## 👤 Author

**Jiangnan Wan**  
📍 M.A. in Statistics, Columbia University  
🔗 [LinkedIn](https://linkedin.com/in/你的链接) | [GitHub](https://github.com/你的主页)

