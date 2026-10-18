# Telecom Customer Churn Prediction

## 1. Project Overview

This project applies machine learning to predict whether a telecom customer is likely to leave their service provider. The goal is to help telecom companies identify customers at risk of churn and support customer-retention decisions.

**Project title:** Predictive Analytics and Explainable Machine Learning Framework for Telecom Customer Churn Prediction

## 2. Objectives

- Analyze customer information from multiple telecom churn datasets.
- Perform data cleaning and exploratory data analysis.
- Prepare numerical and categorical features for machine learning.
- Train and evaluate Logistic Regression, Decision Tree, and Random Forest classifiers.
- Compare models using accuracy, precision, recall, F1-score, and ROC-AUC.
- Generate predictions for previously unseen customer records.

## 3. Datasets

This project currently evaluates three labelled datasets separately:

1. **IBM Telco Customer Churn:** 7,043 original records.
2. **Telecom Data:** 51,047 records.
3. **Customer Churn Prediction 2020:** 4,250 labelled training records and 750 competition test records.

The datasets have different feature schemas and customer populations. Their records are not blindly merged. The 750 competition test records are used to generate predictions, not to calculate accuracy because their true churn labels are unavailable.

## 4. Technologies

- Python
- Jupyter Notebook
- Pandas and NumPy
- Matplotlib and Seaborn
- Scikit-learn
- Joblib
- Visual Studio Code

## 5. Methodology

1. Data collection
2. Data understanding and exploratory analysis
3. Data cleaning and missing-value handling
4. Feature preprocessing and encoding
5. Training/testing split
6. Model training
7. Model evaluation
8. Comparison of model performance
9. Saving trained models
10. Generating predictions

## 6. Machine Learning Algorithms

- Logistic Regression
- Decision Tree Classifier
- Random Forest Classifier

## 7. Evaluation Metrics

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC

Recall and F1-score are important because a model that misses customers who actually churn may be less useful to a telecom company's retention team.

## 8. Initial Experimental Results

The following results were obtained from the current dataset-specific test splits.

| Dataset | Model | Accuracy | Precision | Recall | F1-score | ROC-AUC |
|---|---|---:|---:|---:|---:|---:|
| IBM Telco | Logistic Regression | 0.8038 | 0.6485 | 0.5722 | 0.6080 | 0.8359 |
| IBM Telco | Decision Tree | 0.7335 | 0.4992 | 0.7995 | 0.6146 | 0.8182 |
| IBM Telco | Random Forest | 0.7676 | 0.5535 | 0.6497 | 0.5978 | 0.8146 |
| Telecom Data | Logistic Regression | 0.5793 | 0.3566 | 0.5717 | 0.4392 | 0.6117 |
| Telecom Data | Decision Tree | 0.5920 | 0.3736 | 0.6145 | 0.4647 | 0.6319 |
| Telecom Data | Random Forest | 0.7071 | 0.4831 | 0.2379 | 0.3188 | 0.6586 |
| Churn Prediction 2020 | Logistic Regression | 0.7541 | 0.3295 | 0.7167 | 0.4514 | 0.7926 |
| Churn Prediction 2020 | Decision Tree | 0.9294 | 0.7632 | 0.7250 | 0.7436 | 0.8151 |
| Churn Prediction 2020 | Random Forest | 0.9482 | 0.8800 | 0.7333 | 0.8000 | 0.8887 |

These are preliminary results from the current experiments. Performance may change if the notebook's preprocessing or evaluation procedure changes.

## 9. Dataset 3 Prediction Output

The Dataset 3 Random Forest model generated predictions for all 750 competition test records:

- Predicted to stay: 649
- Predicted to churn: 101

These are predicted labels, not verified customer outcomes.

## 10. Repository Structure

- `data/raw/` — original datasets
- `data/processed/` — generated prediction files
- `models/` — saved machine learning pipelines
- `notebooks/` — Jupyter Notebook
- `reports/` — evaluation metrics, confusion matrix, and charts
- `requirements.txt` — Python dependencies
- `.gitignore` — files excluded from version control

## 11. How to Run

1. Install Python and Visual Studio Code.
2. Open the project folder.
3. Activate the project's virtual environment.
4. Install dependencies using `python -m pip install -r requirements.txt`.
5. Open the notebook in `notebooks/`.
6. Run the cells in order from the beginning.

Ensure that dataset filenames and paths match those used in the notebook. The complete notebook should be tested from a fresh kernel before submission.

## 12. Conclusion

The project demonstrates how machine learning can be applied to telecom customer churn prediction. Comparing three algorithms across three datasets shows that performance depends on the dataset and that accuracy alone is insufficient for model selection. Random Forest achieved the strongest results on the Customer Churn Prediction 2020 test split among the three algorithms evaluated there.

## 13. References

- IBM Telco Customer Churn: https://www.kaggle.com/datasets/blastchar/telco-customer-churn
- Customer Churn Prediction 2020: https://www.kaggle.com/competitions/customer-churn-prediction-2020/data
- Scikit-learn documentation: https://scikit-learn.org/stable/
- Pandas documentation: https://pandas.pydata.org/docs/