# 🏥 Hospital Readmission Risk Prediction

## 📌 Project Overview
This project aims to predict whether a patient will be readmitted to the hospital within 30 days using machine learning techniques. Early prediction can help hospitals reduce costs and improve patient outcomes.

---

## 📊 Dataset
- Source: Diabetes 130-US hospitals dataset
- Size: ~100,000 patient records
- Target variable:
  - `readmit_binary` (1 = readmitted within 30 days, 0 = not)

---

## 🔍 Data Preprocessing
- Converted `readmitted` into binary classification
- Transformed age ranges into numeric values
- Removed ID-related columns (`encounter_id`, `patient_nbr`)
- Selected key clinical and utilization features:
  - number of inpatient visits
  - emergency visits
  - medications
  - insulin usage
  - time in hospital

---

## 🤖 Model
- Logistic Regression
- Handled class imbalance using:
  - `class_weight='balanced'`

---

## 📈 Model Performance

- Accuracy: **0.68**
- Recall (readmitted patients): **0.46**
- F1-score: **0.25**
- AUC: **0.63**

---

## 📊 Visualizations

### 🔹 ROC Curve
![ROC Curve](https://github.com/cindycc88x-neko/hospital-readmission-analysis/blob/main/ROCCurve.png?raw=true)

### 🔹 Feature Importance
![Feature Importance](https://github.com/cindycc88x-neko/hospital-readmission-analysis/blob/main/FeatureImportance.png?raw=true)

### 🔹 Confusion Matrix
![Confusion Matrix](https://github.com/cindycc88x-neko/hospital-readmission-analysis/blob/main/ConfusionMatrix.png?raw=true)

## 💡 Key Insights
- Patients with more inpatient visits are more likely to be readmitted
- Medication usage and insulin treatment show strong influence
- Model has moderate predictive power but highlights important clinical factors

---

## 🚀 Future Improvements
- Try advanced models (Random Forest, XGBoost)
- Feature engineering (comorbidity scores, history patterns)
- Hyperparameter tuning
- Handle imbalance with SMOTE

---

## 🛠️ Tech Stack
- Python
- Pandas
- Scikit-learn
- Matplotlib
