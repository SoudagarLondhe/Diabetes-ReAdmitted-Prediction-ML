## Diabetes Readmission Prediction
This project aims to build a predictive machine learning model that classifies whether a diabetic patient is likely to be readmitted to the hospital within 30 days based on clinical and demographic data. The solution is built using Python and popular ML libraries and is intended to support healthcare providers in identifying high-risk patients to improve care and reduce costs.

## Project Overview
Hospital readmissions are a critical concern in the healthcare system, both from the standpoint of patient care and cost management. This project leverages historical hospital data of diabetic patients from over 130 U.S. hospitals collected between 1999 and 2008. The goal is to:

- Understand key factors contributing to hospital readmission.
- Apply data preprocessing techniques to clean and structure the data.
- Train and evaluate machine learning models to predict patient readmission within 30 days.
- Derive insights that can support proactive patient management strategies.

## Dataset Description
Source: UCI Machine Learning Repository - Diabetes 130-US hospitals ([Link](https://archive.ics.uci.edu/dataset/296/diabetes+130-us+hospitals+for+years+1999-2008))

Dataset Highlights:
- ~100,000 records of diabetic patients
- 50+ features per patient record
- Target variable: readmitted (values: <30, >30, or NO)
- Includes demographic, admission, diagnostic, medication, and lab result data

## Technologies & Libraries Used
- Python: Core programming language
- Pandas & NumPy: Data wrangling and analysis
- Matplotlib & Seaborn: Data visualization
- Scikit-learn: ML algorithms, preprocessing, model selection, and evaluation

## Machine Learning Models
Multiple models were trained and evaluated for classification:
- Logistic Regression: Baseline linear model
- Decision Tree: Captures complex feature interactions
- Random Forest: Ensemble method to improve accuracy and reduce overfitting
- Support Vector Machine (optional): Tried in some iterations depending on kernel type

## Results & Observations
- Feature Importance: Length of stay, number of lab procedures, A1C results, and insulin usage were among the top predictors.
- Model Performance: Random Forest yielded the best F1-score, followed by Decision Tree and Logistic Regression.
- The data imbalance (very few <30 readmission cases) was handled using stratified sampling and evaluation metrics beyond accuracy.
- Visualizations and correlation heatmaps provided insights into feature relationships.

## Future Improvements
- Apply SMOTE or other oversampling techniques for better class balance.
- Hyperparameter tuning using GridSearchCV.
- Deploy the model using Flask for real-time predictions.
- Integrate with EHR systems to provide patient-level readmission risk scores.