# 📊 Feature Selection Report - Stress_Level Prediction for Coffee Health

## ✅ Data Cleaning
- Removed duplicates
- Checked missing values
- Filled `Health_Issues` with mode

---

## 🔎 Exploratory Data Analysis
- Histograms, boxplots, scatterplots, bar charts
- Crosstab + heatmap to explore categorical vs Stress_Level
- Identified imbalance:  
  - Low: ~70%  
  - Medium: ~20%  
  - High: ~10%  

---

## 🧪 Feature Selection

### Categorical Features (Chi-Square Test with Stress_Level)
- Keep features with **p < 0.05**
- Examples: `Gender`, `Country`, `Occupation`, `Health_Issues`, `Smoking`, `Alcohol_Consumption`

### Numerical Discrete (Chi-Square / ANOVA)
- Keep features with **significant association**
- Examples: `Coffee_Intake`, `Physical_Activity_Hours`

### Numerical Continuous (ANOVA Test)
- Keep features with **p < 0.05**
- Examples: `Age`, `Caffeine_mg`, `Sleep_Hours`, `Sleep_Quality`, `BMI`, `Heart_Rate`

---

## 🚀 Next Steps

1. **Encoding**
   - Apply Label Encoding / One-Hot Encoding for categorical variables

2. **Scaling**
   - Use `StandardScaler` or `MinMaxScaler` for continuous features

3. **Model Training**
   - Try models:  
     - Logistic Regression  
     - Random Forest Classifier  
     - XGBoost  
   - Handle class imbalance:  
     - `class_weight='balanced'`  
     - SMOTE oversampling  

4. **Evaluation**
   - Metrics: `precision`, `recall`, `f1-score`, `accuracy`  
   - Use **macro/micro averaging** due to imbalance  
   - Confusion Matrix for visual insights

---

## 🎯 Final Note
Only **features with significant Chi-Square / ANOVA results** should be included in the ML pipeline for predicting `Stress_Level`.
