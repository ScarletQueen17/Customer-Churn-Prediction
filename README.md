#  Customer Churn Prediction

##  Project Overview
This project aims to predict **customer churn** for a bank using machine learning models.  
Customer churn refers to the likelihood of customers leaving the bank, which is a critical problem in the financial sector.  
By predicting churn, the bank can take proactive measures to improve customer retention.

---

##  Dataset
The dataset used contains **10,000 customer records** with the following features:

- **CreditScore**: Credit score of the customer  
- **Geography**: Country of the customer  
- **Gender**: Male or Female  
- **Age**: Age of the customer  
- **Tenure**: Number of years the customer has been with the bank  
- **Balance**: Account balance  
- **NumOfProducts**: Number of bank products purchased  
- **HasCrCard**: Whether the customer has a credit card (1 = Yes, 0 = No)  
- **IsActiveMember**: Whether the customer is active (1 = Yes, 0 = No)  
- **EstimatedSalary**: Estimated annual salary  

**Target Variable**  
- **Exited**: Whether the customer left the bank (1 = Yes, 0 = No)

---

## Steps Taken
1. **Data Preprocessing**  
   - Handled categorical variables with OneHotEncoding  
   - Normalized numerical features  

2. **Balancing the Dataset**  
   - Applied **SMOTE (Synthetic Minority Oversampling Technique)**  
   - Balanced target classes:  
     - Before SMOTE → 0: 6371, 1: 1630  
     - After SMOTE → 0: 6371, 1: 6371  

3. **Model Training**  
   - Logistic Regression  
   - Random Forest Classifier  

4. **Evaluation Metrics**  
   - Accuracy  
   - Precision  
   - Recall  
   - F1-Score  

---

##  Results

### Logistic Regression
- **Accuracy**: 71%  
- **Precision**: 0.38  
- **Recall**: 0.66  
- **F1 Score**: 0.48  

### Random Forest
- **Accuracy**: 85%  
- **Precision**: 0.63  
- **Recall**: 0.59  
- **F1 Score**: 0.61  

 **Random Forest outperformed Logistic Regression.**

---

##  Feature Importance (Random Forest)

| Feature          | Importance |
|------------------|------------|
| Age              | 0.243 |
| IsActiveMember   | 0.173 |
| EstimatedSalary  | 0.097 |
| Balance          | 0.095 |
| NumOfProducts    | 0.092 |
| CreditScore      | 0.087 |
| HasCrCard        | 0.064 |
| Gender           | 0.057 |
| Tenure           | 0.053 |
| Geography        | 0.040 |

---

##  Visualizations
- Feature Importance Plot  
- Comparison of Model Performance  



---

##  Conclusion
- Random Forest performed better than Logistic Regression in predicting churn.  
- The most important factors influencing churn are **Age**, **Activity Level**, and **Salary/Balance**.  
- The bank should focus on **retaining older customers** and **inactive members** to reduce churn.

