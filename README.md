# Heart Disease Prediction Using Machine Learning

## Overview
This project uses machine learning models to predict the likelihood of a heart attack based on patient attributes. 
The dataset contains medical and demographic features, and the target variable indicates the risk of a heart attack 
(1 = higher risk, 0 = lower risk). The goal was to develop an accurate classification model through preprocessing, feature selection, and hyperparameter tuning.

---

## FEATURES
- **Heart Disease Prediction Dataset**: This dataset contains 1,888 records merged from five publicly available heart disease datasets:
- [Heart Disease Dataset on Kaggle]([https://www.kaggle.com/path-to-dataset](https://www.kaggle.com/datasets/mfarhaannazirkhan/heart-dataset/data))
  - age: Age of the patient (Numeric).
  - sex: Gender of the patient. Values: 1 = male, 0 = female.
  - cp: Chest pain type. Values: 0 = Typical angina, 1 = Atypical angina, 2 = Non-anginal pain, 3 = Asymptomatic.
  - trestbps: Resting Blood Pressure (in mm Hg) (Numeric).
  - chol: Serum Cholesterol level (in mg/dl) (Numeric).
  - fbs: Fasting blood sugar > 120 mg/dl. Values: 1 = true, 0 = false.
  - restecg: Resting electrocardiographic results. Values: 0 = Normal, 1 = ST-T wave abnormality, 2 = Left ventricular hypertrophy.
  - thalach: Maximum heart rate achieved (Numeric).
  - exang: Exercise-induced angina. Values: 1 = yes, 0 = no.
  - oldpeak: ST depression induced by exercise relative to rest (Numeric).
  - slope: Slope of the peak exercise ST segment. Values: 0 = Upsloping, 1 = Flat, 2 = Downsloping.
  - ca: Number of major vessels (0-3) colored by fluoroscopy. Values: 0, 1, 2, 3.
  - thal: Thalassemia types. Values: 1 = Normal, 2 = Fixed defect, 3 = Reversible defect.
  - target: Outcome variable (heart attack risk). Values: 1 = more chance of heart attack, 0 = less chance of heart attack.

---

## Methodology
1. **Data Preprocessing**:
   - Handled missing values using appropriate strategies (mode for categorical and binary variables, median for numerical variables).
   - Categorical and binary features were already encoded. Scaled the data using StandardScaler.

2. **Modeling**:
   - Baseline models included LogisticRegression, Random Forest Classifier, XGBoost CLassifier, SVC and KNN.
   - Feature importance analysis highlighted `thal`, `thalachh`, and `oldpeak` as the most influential features.
   - Removed features (`fbs`, `exang`, and `sex`) after feature importance analysis showed they had low predictive importance.
   - Hyperparameter tuning was performed using GridSearchCV to optimize Random Forest and XGBoost models.

3. **Evaluation**:
   - Models were evaluated on validation and test sets, with metrics including accuracy and classification reports.

---

## Results
- **Best Model**: Random Forest (Baseline)
  - Validation Accuracy: **0.95**
  - Test Accuracy: **0.95**
- XGBoost also performed well but had slightly lower accuracy (Test Accuracy: **0.94**).
- Dropping low-importance features improved model performance.

<img width="404" alt="image" src="https://github.com/user-attachments/assets/e062b046-4298-4795-bdc6-09f856334219" />


---

