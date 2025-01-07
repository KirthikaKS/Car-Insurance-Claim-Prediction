**CAR INSURANCE CLAIM PREDICTION**
===
This repository contains the implementation and analysis of the "Car Insurance Claim Prediction". The project utilizes various machine learning models to predict whether a policyholder will file a car insurance claim within six months.
___

**BUSINESS SCNARIO**
===
The insurance industry is undergoing rapid transformation through data analytics and predictive modeling. Car insurance companies strive to refine their risk assessment and pricing strategies by predicting the likelihood of claims being filed by policyholders. By leveraging a comprehensive dataset, this project aims to empower insurance providers with predictive insights, enabling proactive risk management and enhanced operational efficiency.
___

**PROJECT OBJECTIVES**
===

**Data Collection**: Utilize a dataset containing policyholder and vehicle attributes.

**Data Exploration**: Perform exploratory data analysis to understand relationships and distributions.

**Data Preprocessing**: Address missing values, standardize numerical data, and encode categorical variables.

**Model Building**: Train classification models using Random Forest, Logistic Regression, Decision Trees, and Neural Networks.

**Evaluation**: Assess model performance using metrics such as accuracy and AUC-ROC.

**Insights**: Gather actionable insights to improve predictive power and model interpretability.
___

**DATASET OVERVIEW**
===

The dataset, sourced from Kaggle, comprises 43 attributes such as policy tenure, vehicle characteristics, and demographic information. The target variable is is_claim, indicating whether a claim was filed (binary classification).

___

**KEY PROCESSING STEPS**
===

**Missing Value Treatment**: Addressed missing values by data imputation techniques tailored to the nature of the data (e.g., mean, median, and mode substitution).

**Feature Transformation**: Derived new features, such as the ratio of max_torque to RPM and max_power to RPM, to capture nuanced patterns in vehicle performance.

**Categorical Encoding**: Converted binary categorical variables into numeric values (0 and 1) and created dummy variables for multi-class categorical attributes using one-hot encoding.

**Standardization**: Ensured numerical variables were standardized to improve model convergence during training.

**Class Imbalance Handling**: Applied oversampling techniques to balance the dataset, ensuring both claim and no-claim classes were equally represented.

![image](https://github.com/user-attachments/assets/7d6b4778-a07d-4730-8a82-4a3ac5498f92)

![image](https://github.com/user-attachments/assets/90737874-6a57-4867-ae8c-83329e40b707)

___

**EXPLORATORY DATA ANALYSIS (EDA)**
===

EDA was conducted to gain a thorough understanding of the dataset:

**Data Structure Analysis**: Reviewed data types, identified categorical and numerical variables, and summarized the distribution of key attributes.

**Target Variable Distribution**: Created pie charts and bar plots to illustrate the significant imbalance between claims (6.4%) and no-claims (93.6%).

**Correlation Analysis**: Analyzed the relationships between predictors and the target variable using correlation matrices and heatmaps.

**Visualizing Categorical Variables**: Generated count plots for variables like area_cluster, segment, model, and fuel_type to identify patterns and relationships with the claim status.

**Numerical Feature Analysis**: Investigated distributions and outliers in numerical features such as policy_tenure and vehicle age using boxplots and histograms.

**Feature Insights**: Highlighted significant patterns, such as older vehicles and specific fuel types being more prone to claims.

![image](https://github.com/user-attachments/assets/3484b560-8129-48c9-9b4c-84b9193db471)

___

**MODELS AND RESULTS**
===

**1. RANDOM FOREST**

![image](https://github.com/user-attachments/assets/b222c6db-6b1e-414e-bc84-3f12da25378f)

![image](https://github.com/user-attachments/assets/f0a8ec0e-04f8-4d2f-9fa0-ce84b4190da0)

Implementation: Trained models with 10, 100, and 500 trees.

Best Accuracy: 61.62%

AUC: 0.6316

**Key Observations:**

Achieved moderate performance with an ability to identify "No Claim" instances better than "Claim" instances.

Variable importance plots revealed policy tenure and vehicle type as significant predictors.
___

**2. LOGISTIC REGRESSION**

![image](https://github.com/user-attachments/assets/702f8140-e79f-49a5-bb79-63e4b0a783bd)

Implementation: Built a binary logistic regression model to evaluate the relationship between predictors and the target variable.

Accuracy: 82.19%

AUC: 0.6128

**Key Observations:**

Provided interpretable results, with significant predictors including policy tenure and vehicle age.

Struggled to accurately classify "Claim" instances due to class imbalance but this was resolved by oversampling. Out of all the techniques logistic regression was more accurate in the prediction.

___

**3. DECISION TREE**

![image](https://github.com/user-attachments/assets/d08c8aaa-bb01-4330-85c7-62d0462d116d)


Implementation: Developed decision trees with varying complexity using the rpart algorithm.

Best Accuracy: 46.37%

AUC: 0.6109

**Key Observations:**

Default trees achieved moderate accuracy.

Deeper trees overfitted the training data, while pruned trees offered a better balance between complexity and generalizability.

___

**4. NEURAL NETWORK**

![image](https://github.com/user-attachments/assets/959780e1-79af-488c-b4a4-b94f855f0331)

Implementation: Tested neural network models with 5 and 10 hidden nodes.

Best Accuracy: 76.71%

AUC: 0.5118

**Key Observations:**

The model's performance improved with an increased network size but remained limited in specificity.

Highlighted the need for architectural optimization and advanced feature selection.
___

**PERFORMANCE OVERVIEW**
===

![image](https://github.com/user-attachments/assets/58fd9eb7-5140-4844-92a6-cd7febdea3f7)

___


**CONCLUSION**
===

This project demonstrates the application of machine learning in the insurance domain, highlighting the trade-offs between the accuracy, interpretability, and generalizability. Logistic Regression emerged as the top-performing model in terms of accuracy, while Random Forest offered better AUC scores, indicating superior discriminatory ability. Despite some limitations, these models provide valuable insights into claim prediction, forming a solid foundation for further refinement and deployment in real-world scenarios.

