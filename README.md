# Car Insurance Claim Prediction

## Introduction
This project focuses on predicting whether policyholders will file a claim in the next six months using a comprehensive dataset. By leveraging advanced analytics and machine learning, the project aims to revolutionize how insurance companies assess risk and determine pricing strategies. 

---

## Goal
The primary objective is to develop an accurate predictive model using policyholder attributes, enabling data-informed decision-making. 

---

## Data Overview
- **Source**: [Kaggle](https://www.kaggle.com/)
- **Dataset**: Contains 97,656 instances and 43 attributes.
- **Attributes**:
  - Policyholder details: policy tenure, age of the car, car owner age.
  - Environmental factors: population density of the city.
  - Vehicle specifics: make and model, power, engine type, max torque, max power.
- **Target Variable**: Indicates whether a policyholder will file a claim (Yes/No) - 'is_claim’
- **Split Ratio**: 60% training and 40% testing. This is a classification problem, and we have used four different algorithms - Logistic Regression, 
Decision Trees, Random Forests, and Neural Networks - to predict the loan status
- ![image](https://github.com/user-attachments/assets/8948f470-1d8d-4598-ac40-a32564c3026a)


---

## Exploratory Data Analysis
- ![image](https://github.com/user-attachments/assets/cd33340e-7e31-4930-8fe8-20a85a86d286)

### Steps Taken:
1. **Handling Missing Values**:
   - Identified and managed null values in the dataset.

2. **Feature Selection**:
   - Dropped irrelevant attributes for classification analysis.

3. **Data Transformation**:
   - Encoded categorical values into numerical form (“No” and “Yes” transformed to 0 and 1).

4. **Feature Engineering**:
   - Grouped attributes into categorical and numerical categories.
   - Extracted numerical values from `Max Torque` and `Max Power` attributes to compute ratios with RPM values.
   - Added new columns by splitting categorical data.

---

## Machine Learning Models
1. **Decision Tree**
   ![Decision Tree](./images/decision_tree.png)


2. **Random Forest**
   ![Random Forest](./images/random_forest.png)

3. **Logistic Regression**
   ![Logistic Regression](./images/logistic_regression.png)

4. **Neural Network**
   ![Neural Network](./images/neural_network.png)

---

## Summary of Results
- **Logistic Regression**:
  - Achieved the highest accuracy among all models.
  - Low AUC indicates room for improvement in distinguishing between classes.

- **Random Forest**:
  - Accuracy was lower than logistic regression.
  - High AUC shows better discrimination between positive and negative cases.
  - Less interpretable compared to logistic regression.

- **Decision Tree**:
  - Prone to overfitting, leading to challenges in generalizing to new data.

---

## Insights and Business Impact
- Identified key policyholder attributes influencing claim likelihood.
- Helps insurance companies refine risk assessment and optimize pricing strategies.
- Offers actionable insights for managing risk effectively in the car insurance industry.

---

## Future Scope
- Enhance the dataset with additional attributes to improve predictive power.
- Explore advanced techniques like hyperparameter tuning and ensemble models.
- Investigate other interpretability methods to better understand model behavior.
