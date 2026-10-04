# iPhone Resale Price Prediction | Machine Learning

## Project Overview

This project uses Machine Learning to predict the resale/current price of iPhones based on their specifications, condition, storage, model, availability, and other market-related features.

The project covers the complete machine learning workflow, from data cleaning and exploratory analysis to preprocessing, model training, evaluation, cross-validation, hyperparameter tuning, and price prediction on new iPhone data.

---

## Objectives

* Analyze factors affecting iPhone resale prices
* Clean and preprocess the dataset
* Convert categorical features into machine-readable form
* Build and compare multiple regression models
* Evaluate models using regression metrics
* Apply Cross-Validation
* Perform Hyperparameter Tuning using GridSearchCV
* Identify important features affecting price
* Predict the price of a new iPhone

---

## Dataset

The dataset contains information about iPhones including:

* Model
* Battery Health
* Battery Renewal
* Screen Replacement
* Display Replacement
* Storage
* Colour
* Release Date
* Backglass Damages
* Screen Damages
* Availability
* iOS Updates
* Months Since Release
* Price Date
* Exchange Rate
* Current Price (LKR)

### Target Variable

`current_price(LKR)`

The target represents the current iPhone price in Sri Lankan Rupees.

---

## Machine Learning Workflow

### 1. Data Understanding

* Dataset shape and structure
* Data types
* Missing values
* Duplicate records
* Unique values
* Basic statistical analysis

### 2. Data Cleaning

* Removed irrelevant identifying information
* Handled categorical values
* Checked missing values
* Prepared features for machine learning

### 3. Exploratory Data Analysis

Analyzed relationships between iPhone prices and:

* iPhone model
* Storage capacity
* Battery health
* Device condition
* Months since release
* Availability
* Other device characteristics

### 4. Feature Preparation

The dataset was divided into:

* Numerical features
* Categorical features

Categorical features were encoded using `OneHotEncoder`.

Numerical features were standardized using `StandardScaler`.

A `ColumnTransformer` was used to apply the appropriate preprocessing to different feature types.

### 5. Train-Test Split

The dataset was divided into training and testing sets using:

```python
train_test_split(
    X,
    y,
    test_size=0.2,
    random_state=42
)
```

### 6. Machine Learning Models

The following regression models were trained and compared:

* Linear Regression
* Decision Tree Regressor
* Random Forest Regressor

### 7. Model Evaluation

The models were evaluated using:

* Mean Absolute Error (MAE)
* Root Mean Squared Error (RMSE)
* R² Score

### 8. Cross-Validation

5-fold Cross-Validation was used to evaluate model performance across multiple train-validation splits.

### 9. Hyperparameter Tuning

`GridSearchCV` was used to find better Random Forest parameters.

Parameters tuned included:

* Number of estimators
* Maximum tree depth
* Minimum samples required for splitting
* Minimum samples required at a leaf

### 10. Feature Importance

Feature importance from the optimized Random Forest model was analyzed to understand which factors contributed most to price prediction.

### 11. New Price Prediction

The final model was also used to predict the price of a new iPhone based on its specifications and condition.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Joblib
* Jupyter Notebook

---

## Key Machine Learning Concepts

This project demonstrates practical knowledge of:

* Regression
* Train-Test Split
* Feature Preprocessing
* One-Hot Encoding
* Feature Scaling
* Pipelines
* ColumnTransformer
* Linear Regression
* Decision Trees
* Random Forest
* MAE
* RMSE
* R² Score
* Cross-Validation
* GridSearchCV
* Hyperparameter Tuning
* Feature Importance

---

## Project Results

Model performance was compared using MAE, RMSE, and R² to identify the most suitable regression model for iPhone price prediction.

The optimized Random Forest model was further evaluated and used for predictions on new iPhone data.

### Model Comparison

| Model               |        MAE |       RMSE |         R² |
| ------------------- | ---------: | ---------: | ---------: |
| Linear Regression   | Add Result | Add Result | Add Result |
| Decision Tree       | Add Result | Add Result | Add Result |
| Random Forest       | Add Result | Add Result | Add Result |
| Tuned Random Forest | Add Result | Add Result | Add Result |

---

## Visualizations

### Model Comparison

![Model Comparison](images/model-comparison.png)

### Actual vs Predicted Prices

![Actual vs Predicted](images/actual-vs-predicted.png)

### Feature Importance

![Feature Importance](images/feature-importance.png)

---

## Example Prediction

The trained model can be used to predict the price of a new iPhone by providing information such as:

* Model
* Battery Health
* Storage
* Device Condition
* Screen Condition
* Availability
* Release Information
* Exchange Rate

Example:

```python
predicted_price = best_model.predict(new_iphone)

print("Predicted iPhone Price (LKR):", predicted_price[0])
```

---

## Project Structure

```text
iphone-resale-price-prediction-ml/
│
├── data/
├── notebooks/
├── images/
├── model/
├── requirements.txt
├── README.md
└── .gitignore
```

---
## Conclusion
This project demonstrates an end-to-end Machine Learning workflow for a real-world regression problem.
The project focuses not only on model training, but also on data preprocessing, categorical encoding, feature scaling, model comparison, cross-validation, hyperparameter optimization, and interpreting model predictions.
---
## Author
**Muhammad Ali Aslam**
Aspiring Data Analyst
GitHub: `malikALIaslam`
LinkedIn: `muhammad-ali-89192535a`
