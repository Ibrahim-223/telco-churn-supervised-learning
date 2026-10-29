# Telco Customer Churn Prediction

## Project Overview
This project predicts whether a telecom customer may leave the company using supervised machine learning.

## Dataset
IBM Telco Customer Churn Dataset:  
https://www.kaggle.com/datasets/blastchar/telco-customer-churn

## Models Used
- Naive Bayes
- K-Nearest Neighbors (KNN)
- Decision Tree
- Support Vector Machine (SVM)

## Project Files
- `CustomerChurn_SupervisedLearning.ipynb` – Complete notebook with code and results.
- `churn_model.pkl` – Saved machine learning pipeline.
- `summary_report.md` – Project summary and findings.
- `requirements.txt` – Required Python libraries.

## How to Run
1. Install Python.
2. Install the required libraries:

   `pip install -r requirements.txt`

3. Open the notebook in Jupyter Notebook.
4. Run the notebook cells in order.
5. Load the saved model using joblib.

## Evaluation
The models are compared using accuracy, precision, recall, F1-score, and ROC-AUC.

## Conclusion
This project demonstrates how supervised machine learning can help identify customers who may leave a telecom company.
