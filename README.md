Here is a complete `README.md` file formatted for your machine learning practice project based on the provided notebook code.

---

# Customer Purchase Prediction

## Overview

This project focuses on analyzing customer data to predict purchasing behavior. It includes complete Exploratory Data Analysis (EDA) and the implementation of multiple machine learning models to classify whether a customer will make a purchase.

## Dataset

The project uses a dataset named `customer_purchase_data.csv`. The raw data contains 1500 records and the following 9 columns:

* **Features:** `Age`, `Gender`, `AnnualIncome`, `NumberOfPurchases`, `ProductCategory`, `TimeSpentOnWebsite`, `LoyaltyProgram`, `DiscountsAvailed`.


* **Target Variable:** `PurchaseStatus` (Binary classification: 0 or 1).



## Project Workflow

### 1. Exploratory Data Analysis (EDA) & Cleaning

* **Data Inspection:** Checked for data types, missing values (0 nulls found), and overall data shape.


* **Data Cleaning:** Identified and removed 112 duplicate rows to ensure data quality.


* **Visualizations:**
* Generated histograms to understand numerical distributions, such as `AnnualIncome`.


* Created a correlation matrix to analyze relationships between variables.


* Plotted a count plot for the target variable `PurchaseStatus` to check for class imbalances.




* **Export:** The cleaned dataset was saved as `purchase.csv` in the processed data directory.



### 2. Data Preprocessing

* **Feature Selection:** The `Gender` column was dropped prior to model training.


* **Data Splitting:** The dataset was divided into training and testing sets using an 80/20 split.


* **Scaling:** Applied `StandardScaler` to the training and testing features to normalize the data for better model convergence.



### 3. Modeling & Evaluation

Three different classification algorithms were developed and evaluated:

* **Logistic Regression:** Achieved an accuracy of roughly 85%. The model was exported as a `.pkl` file for future use.


* **Random Forest Classifier:** Configured with 100 estimators, this model performed the best with an accuracy of approximately 90%. It was also saved as a `.pkl` file.


* **Neural Network:** Built a sequential model using TensorFlow/Keras featuring three Dense layers: an input layer (32 neurons, ReLU activation), a hidden layer (16 neurons, ReLU activation), and an output layer (1 neuron, Sigmoid activation).



## Repository Structure

* `../data/raw/` - Contains the raw input data (`customer_purchase_data.csv`).


* `../data/processed/` - Contains the cleaned dataset ready for modeling (`purchase.csv`).


* `../notebooks/` - Contains the Jupyter notebooks for EDA, Logistic Regression, Random Forest, and Neural Network experiments.


* `../models/` - Directory storing the serialized machine learning models (`logistic_regression_model.pkl`, `random_forest_model.pkl`).