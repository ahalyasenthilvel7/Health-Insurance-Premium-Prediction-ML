# Health Insurance Premium Prediction Using Machine Learning

## 📌 Project Overview

This project focuses on predicting **health insurance charges** based on customer-related features such as age, BMI, number of children, gender, smoking status, and region.

The project compares **five different regression models** and evaluates their performance using **Mean Squared Error (MSE)** and **R-squared (R²)**.

After comparing the models, the **Random Forest Regressor** was selected as the final model because it achieved the best performance on unseen test data.

---

## 🎯 Objective

The main objective of this project is to:

- Predict health insurance charges for a given individual.
- Understand how different features affect insurance charges.
- Compare multiple regression algorithms.
- Identify the model that performs best on unseen data.
- Use the selected model to predict charges for new individuals.

---

## 📊 Dataset Features

The dataset contains the following important features:

| Feature | Description |
|---|---|
| **Age** | Age of the individual |
| **BMI** | Body Mass Index |
| **Children** | Number of children/dependents |
| **Sex** | Gender of the individual |
| **Smoker** | Smoking status |
| **Region** | Residential region |
| **Charges** | Health insurance charge/premium |

### Target Variable

**Charges** is the target variable that the machine learning models are trained to predict.

---

## 🔄 Machine Learning Workflow

The project follows these major steps:

1. **Load the dataset**
2. **Understand the dataset**
3. **Perform data exploration**
4. **Analyze categorical and numerical features**
5. **Prepare the input and target variables**
6. **Encode categorical features**
7. **Split the dataset into training and testing sets**
8. **Build multiple regression models**
9. **Evaluate each model using MSE and R²**
10. **Compare model performance**
11. **Select the best-performing model**
12. **Predict insurance charges for unseen data**
13. **Analyze feature impact**
14. **Provide business recommendations**

---

## 🧹 Data Preprocessing

The categorical features were converted into numerical form before training the models.

The encoded features include:

- **sex_male**
- **smoker_yes**
- **region_northwest**
- **region_southeast**
- **region_southwest**

The dataset was divided into:

- **Training data** → Used to train the models
- **Testing data** → Used to evaluate how well the models perform on unseen data

---

# 🤖 Models Used

Five regression models were developed and compared.

## Model 1: Linear Regression – Age Only

The first model uses only **Age** as the input feature.

### Result

- **Train MSE:** 1.246248 × 10⁸
- **Train R²:** 0.082229
- **Test MSE:** 1.545219 × 10⁸
- **Test R²:** 0.096985

### Observation

Age alone has limited ability to predict insurance charges.

---

## Model 2: Linear Regression – Age + BMI

The second model uses:

- Age
- BMI

### Result

- **Train MSE:** 1.222942 × 10⁸
- **Train R²:** 0.099392
- **Test MSE:** 1.471034 × 10⁷
- **Test R²:** 0.140338

### Observation

Adding BMI improves the model slightly, but the predictive performance is still limited.

---

## Model 3: Linear Regression – All Features

The third model uses all available features.

### Result

- **Train MSE:** 3.581293 × 10⁷
- **Train R²:** 0.736264
- **Test MSE:** 3.894017 × 10⁷
- **Test R²:** 0.772436

### Observation

Using all features significantly improves the prediction performance.

The train and test scores are relatively close, indicating good generalization.

---

## Model 4: Decision Tree Regressor

A Decision Tree Regressor was trained using all features.

### Result

- **Train MSE:** 0
- **Train R²:** 1.000000
- **Test MSE:** 3.849066 × 10⁷
- **Test R²:** 0.775063

### Observation

The model fits the training data perfectly but performs considerably less perfectly on unseen data.

This indicates **overfitting**.

Therefore, this model was not selected as the final model.

---

## Model 5: Random Forest Regressor ⭐

The Random Forest Regressor was trained using all available features.

### Result

- **Train MSE:** 3.522529 × 10⁶
- **Train R²:** 0.974059
- **Test MSE:** 2.334243 × 10⁷
- **Test R²:** 0.863588

### Observation

Random Forest achieved the **highest test R²** and the **lowest test MSE** among the five models.

Therefore, it was selected as the **final model**.

---

# 📈 Model Comparison

| Model | Train MSE | Train R² | Test MSE | Test R² |
|---|---:|---:|---:|---:|
| **Model 1 – Age Only** | 1.246248 × 10⁸ | 0.082229 | 1.545219 × 10⁸ | 0.096985 |
| **Model 2 – Age + BMI** | 1.222942 × 10⁸ | 0.099392 | 1.471034 × 10⁸ | 0.140338 |
| **Model 3 – All Features** | 3.581293 × 10⁷ | 0.736264 | 3.894017 × 10⁷ | 0.772436 |
| **Model 4 – Decision Tree** | 0 | 1.000000 | 3.849066 × 10⁷ | 0.775063 |
| **Model 5 – Random Forest** ⭐ | 3.522529 × 10⁶ | 0.974059 | **2.334243 × 10⁷** | **0.863588** |

---

# 🏆 Final Model Selection

**Random Forest Regressor** was selected as the final model.

### Why Random Forest?

- **Highest Test R²:** 0.863588
- **Lowest Test MSE:** 2.334243 × 10⁷
- Performs well on **unseen data**
- Provides better predictive performance than the other tested models
- Shows a good balance between training and testing performance

### Final Model Performance

> **Test R² = 0.863588**

This means the model explains approximately **86.36% of the variation in insurance charges** in the test dataset.

---

# 🔍 Feature Impact on Health Insurance Charges

Based on the Linear Regression model with all features:

### **1. Age ↑ → Charges ↑**

- As age increases, insurance charges generally increase.
- Approx. **+$251 for every 1-year increase** in the Linear Regression model.

### **2. BMI ↑ → Charges ↑**

- Higher BMI generally leads to higher insurance charges.
- Approx. **+$328 for every 1-unit increase** in BMI in the Linear Regression model.

### **3. Children ↑ → Charges ↑**

- As the number of children increases, charges generally increase.
- Approx. **+$522 for every additional child** in the Linear Regression model.

### **4. Smoker: No → Yes → Charges ↑↑**

- Smoking has the **strongest impact** among the features in the Linear Regression model.
- Approx. **+$22,874 for smokers compared with non-smokers**.

### **5. Gender → Small Difference**

- Gender has a relatively small effect compared with smoking, BMI, and age.

### **6. Region → Small Impact**

- Region affects charges slightly.
- Its impact is smaller compared with smoking, BMI, and age.

### **7. Age ↑ + BMI ↑ → Charges generally ↑**

- When both age and BMI increase, insurance charges generally tend to increase.

### **8. Age ↑ + Smoker = Yes → Charges can increase significantly**

- Smoking combined with increasing age can result in substantially higher predicted charges.

### **9. BMI ↑ + Smoker = Yes → Charges can increase significantly**

- Higher BMI combined with smoking is generally associated with higher charges.

> **Note:** The approximate dollar values above are based on the coefficients of the **Linear Regression Model 3**. The final Random Forest model does not have one fixed dollar effect for each feature.

---

# 🔮 Prediction on Unseen Data

The final **Random Forest Regressor** was used to predict insurance charges for unseen individuals.

For example, the notebook demonstrates prediction using an individual with:

- **Age:** 30
- **BMI:** 25
- **Children:** 0
- **Gender:** Male
- **Smoker:** No
- **Region:** Northwest

The trained Random Forest model predicts the expected insurance charge based on these input features.

---

# 💼 Business Recommendations

### **1. Targeted Premium Pricing**

Adjust insurance premiums based on factors such as age and BMI to better reflect customer risk.

### **2. Smoking Cessation Incentives**

Offer discounts or wellness rewards to encourage non-smoking behavior and potentially reduce insurance costs.

### **3. Wellness Programs**

Promote healthy lifestyle choices and BMI management to support lower health risks and future claims.

### **4. Region-Based Strategy**

Since region has a relatively limited impact, region-specific pricing should be considered only when supported by operational or risk differences.

### **5. Marketing Focus**

Focus on younger individuals, non-smokers, and customers with healthier BMI levels for affordable plans while providing suitable coverage options for higher-risk customers.

---

# 🛠️ Technologies Used

- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **Scikit-learn**
- **Jupyter Notebook / Google Colab**

---

# 📚 Machine Learning Concepts Used

- Exploratory Data Analysis (EDA)
- Data Preprocessing
- Categorical Encoding
- Train-Test Split
- Linear Regression
- Decision Tree Regression
- Random Forest Regression
- Mean Squared Error (MSE)
- R-squared (R²)
- Model Comparison
- Overfitting Analysis
- Prediction on Unseen Data

---

# 📌 Conclusion

This project demonstrates how machine learning can be used to predict health insurance charges using customer information.

Five different regression models were developed and evaluated. While the Decision Tree achieved perfect training performance, it showed signs of overfitting.

The **Random Forest Regressor** achieved the best overall performance, with a **Test R² of 0.863588** and a **Test MSE of 2.334243 × 10⁷**.

Therefore, **Random Forest Regressor was selected as the final model for health insurance premium prediction.**

---

## 👩‍💻 Project Author

**Ahalya S**

*Machine Learning Project – Health Insurance Premium Prediction*
