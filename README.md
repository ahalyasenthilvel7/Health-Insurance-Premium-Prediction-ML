# Health-Insurance-Premium-Prediction-ML
Health Insurance Premium Prediction Using Machine Learning

**Project Overview**

Health insurance premiums vary based on several personal and lifestyle factors. This project develops a Machine Learning model to predict health insurance charges using customer information such as age, gender, BMI, smoking status, number of children, and region. The objective is to help insurance providers estimate premium costs accurately and support data-driven decision-making.

**Objective**

* Predict health insurance premiums using machine learning.
* Analyze the impact of customer features on insurance charges.
* Compare the performance of different machine learning algorithms.
* Build a reliable model for premium estimation.

**Dataset**

The dataset contains 1,338 customer records with the following features:
* Age
* Gender
* BMI
* Number of Children
* Smoking Status
* Region
* Insurance Charges (Target Variable)
  
**Technologies Used**

* Python
* NumPy
* Pandas
* Matplotlib
* Seaborn
* Scikit-learn

**Project Workflow**

* Data Loading
* Exploratory Data Analysis (EDA)
* Data Preprocessing
* Feature Encoding
* Train-Test Split
* Model Training
* Model Evaluation
* Premium Prediction

**Machine Learning Models**

**1. Linear Regression**
Built a regression model to predict insurance charges.
Evaluated using Mean Squared Error (MSE) and R² Score.
Achieved an R² Score of approximately 0.77, providing good prediction performance.

**2. Decision Tree Regressor**
Implemented a Decision Tree Regression model for comparison.
The model showed overfitting, with excellent performance on the training data but poor generalization on the test data.
Therefore, Linear Regression was selected as the final model because it produced more consistent and reliable predictions on unseen data.

**Results**

Best Model: Linear Regression
R² Score: ~0.77
Successfully predicted insurance premiums using customer demographic and health-related features.
Demonstrated the importance of proper model selection by comparing Linear Regression with Decision Tree Regression.

**Key Features**

* Comprehensive Exploratory Data Analysis (EDA)
* Data preprocessing and feature encoding
* Multiple machine learning model implementation
* Model performance comparison
* Insurance premium prediction for new customer data
  
**Conclusion**

This project demonstrates how machine learning can be applied to predict health insurance premiums. Multiple algorithms were evaluated, including Linear Regression and Decision Tree Regression. Although the Decision Tree model suffered from overfitting, Linear Regression provided better generalization and more reliable predictions, making it the preferred model for this dataset.
