{
 "cells": [
  {
   "cell_type": "markdown",
   "id": "7356b454-367d-4a27-a76d-5130a5442142",
   "metadata": {},
   "source": [
    "# Customer Churn Prediction – Summary Report\n",
    "\n",
    "## 1. Business Problem and Dataset\n",
    "\n",
    "Customer churn means when a customer stops using a company's services. Losing customers can reduce the company's income. The main goal of this project is to predict which customers may leave the company.\n",
    "\n",
    "In this project, we used the IBM Telco Customer Churn dataset. It contains 7,043 customer records and 21 columns. The dataset includes customer details, services, contract types, monthly charges, tenure, and churn status. There are 1,869 customers who left the company and 5,174 customers who stayed.\n",
    "\n",
    "## 2. Data Preprocessing and Class Imbalance\n",
    "\n",
    "First, we checked the dataset for missing values, duplicate records, and data types. We removed the customer ID column because it does not help predict churn. We converted `TotalCharges` into numeric format and filled missing values.\n",
    "\n",
    "We also created new features, such as tenure groups, number of services, and automatic payment status. We converted categorical data into numeric format using encoding and scaled the numerical features.\n",
    "\n",
    "The dataset was imbalanced because the number of customers who stayed was much higher than the number who left. We used SMOTE to create more examples of the minority class in the training data. We also tested class weights to help the model identify customers who may leave.\n",
    "\n",
    "## 3. Model Comparison and Recommendation\n",
    "\n",
    "We tested four machine learning models: Naive Bayes, KNN, Decision Tree, and SVM.\n",
    "\n",
    "Based on our results, I recommend the **Naive Bayes model** because it achieved the highest recall of **80.75%**. Its precision was 47.78%, F1-score was 60.04%, and AUC-ROC was 82.00%.\n",
    "\n",
    "Recall is important because it tells us how many actual churn customers the model correctly identifies. A higher recall helps the company find more customers who may leave and contact them before they leave. However, the model can also identify some customers incorrectly, so its predictions should be checked carefully.\n",
    "\n",
    "## 4. Top Three Churn Signals and Business Actions\n",
    "\n",
    "The Decision Tree model identified these important churn signals:\n",
    "\n",
    "1. **Month-to-month contract:** This was the most important feature. The company should offer long-term contract benefits and discounts to these customers.\n",
    "2. **Customer tenure:** How long a customer has stayed with the company is an important signal. The company should give new customers better support and welcome offers.\n",
    "3. **Fiber optic internet service:** This feature helped the model predict churn. The company should check customer satisfaction, internet speed, service quality, and complaints.\n",
    "\n",
    "These features help identify possible churn patterns, but they do not prove that every customer with these features will leave.\n",
    "\n",
    "## 5. Future Improvements\n",
    "\n",
    "In the future, I would collect more customer data, including complaints, service quality, and customer feedback. I would also test more models and improve the model's precision and recall.\n",
    "\n",
    "Deep learning could be tested later if we have enough useful data. Finally, I would create a real-time scoring API using FastAPI. It could accept customer details and return the churn probability. The retention team could use these predictions to contact high-risk customers and offer suitable solutions.\n",
    "\n",
    "## Conclusion\n",
    "\n",
    "This project shows how machine learning can help predict customer churn. The Naive Bayes model is recommended because it found the highest number of actual churn customers among the tested models. The company can use these predictions to improve customer satisfaction and reduce customer loss."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "4292720c-2904-4f6c-a18b-98c885759a89",
   "metadata": {},
   "outputs": [],
   "source": []
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3 (ipykernel)",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.13.9"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 5
}
