📊 Insights Report – Logistic Regression on Census Income Data
📌 Project Objective
The objective of this project is to predict whether an individual earns more than $50K per year based on demographic, occupational, and financial attributes using Logistic Regression.

📁 Dataset Overview
Source: 1994 U.S. Census Bureau database

Rows: ~32,000 observations

Features: 15+ including:

age, workclass, education, marital-status, occupation, race, sex, capital-gain, capital-loss, hours-per-week, native-country, etc.

Target Variable: Annual_Income — with values:

<=50K

>50K

🧹 Data Cleaning & Preprocessing Performed
✅ Removed 24 duplicate records

✅ Replaced placeholder values ('?') with NaN and dropped missing rows

✅ Stripped whitespaces in all categorical string columns

✅ Identified and analyzed outliers in numerical columns

✅ Checked feature correlation using a heatmap

✅ Converted target to binary:

0 for income ≤50K

1 for income >50K

✅ Applied one-hot encoding to categorical variables using pd.get_dummies()

✅ Scaled numerical features using StandardScaler to improve convergence in logistic regression

⚙️ Model Used
Model: Logistic Regression

Hyperparameters: max_iter = 1000

Solver: lbfgs (default)

Scaling: StandardScaler applied to all numeric columns

📈 Model Performance
Metric	Score
Accuracy	85.05%
Precision (>50K)	76%
Recall (>50K)	62%
F1-Score (>50K)	68%

🔍 Key Insights
The model performs well as a baseline classifier with over 85% accuracy.

High precision for identifying >50K earners, though recall is lower, indicating some high earners are being missed.

Class imbalance exists — more people earn ≤50K, which affects recall.

Applying feature scaling helped eliminate convergence warnings from the logistic regression solver.

🚀 Recommendations for Improvement
Apply class balancing methods like:

class_weight='balanced'

SMOTE (Synthetic Minority Oversampling)

Try more advanced models:

Random Forest, XGBoost, or SVM

Evaluate model using:

ROC Curve and AUC Score

Analyze feature importance to find top predictors of income

✅ Conclusion
Logistic Regression served as a solid and interpretable starting point. With further enhancements and techniques, this model can evolve into a production-grade income prediction tool for use in economic, social, or policy decision-making contexts.

