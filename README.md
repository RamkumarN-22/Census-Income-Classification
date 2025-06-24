# Logistic Regression: Census Income Classification

This project uses the U.S. 1994 Census Income dataset to build a Logistic Regression model that classifies individuals based on their likelihood of earning over $50K annually.

---

## 📌 Project Goal

To predict whether an individual earns **more than $50K** or **less than or equal to $50K** per year using demographic and work-related attributes.

---

## 🧹 Data Cleaning & Exploratory Data Analysis (EDA)

- ✅ Removed **duplicate rows** (24 identified)
- ✅ Replaced **placeholder values (`'?'`)** with `NaN`, then dropped missing rows
- ✅ Stripped **leading/trailing whitespaces** in string columns
- ✅ Detected **outliers** using boxplots for numerical features
- ✅ Generated a **correlation heatmap** to understand feature relationships
- ✅ Converted target to binary:
  - `0` for income ≤50K
  - `1` for income >50K
- ✅ Applied **one-hot encoding** to all categorical features
- ✅ Standardized all numerical columns using `StandardScaler`

---

## 🤖 Model Details

- **Algorithm Used:** Logistic Regression
- **Hyperparameter:** `max_iter=1000`
- **Feature Scaler:** `StandardScaler` (for improving convergence)

---

## 📈 Model Performance

| Metric             | Score     |
|--------------------|-----------|
| Accuracy           | **85.05%** |
| Precision (>50K)   | 76%       |
| Recall (>50K)      | 62%       |
| F1 Score (>50K)    | 68%       |

The model classifies lower-income individuals (≤50K) more accurately than high-income ones, which is common in imbalanced datasets.

---

## 🔍 Evaluation Summary

- Model performed well as a **baseline classifier**.
- **Convergence warnings** were resolved by applying **feature scaling**.
- **False negatives** exist in the high-income group, indicating possible class imbalance.
- The model can benefit from improvements like advanced models or class rebalancing.

---

## 🚀 Future Improvements

- Use `class_weight='balanced'` or **SMOTE** to handle class imbalance
- Experiment with **Random Forest**, **XGBoost**, or **SVM** models
- Plot **ROC Curve** and calculate **AUC score**
- Explore **feature importance** to identify key drivers of income

---

## 📄 Detailed Summary

Please refer to the `Insights_Report_CensusIncome.pdf` for full project insights, steps, and interpretation.
