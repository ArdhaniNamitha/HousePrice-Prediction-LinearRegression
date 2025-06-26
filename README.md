# HousePrice-Prediction-LinearRegression
Predicting house prices using Linear Regression. Includes data preprocessing, model training, and performance evaluation with MAE, MSE, and R² metrics.

## Purpose of the Project

The goal of this project is to understand how different factors influence house pricing and to build a predictive model that can estimate the price of a house based on its attributes. This is useful for learning the fundamentals of regression, as well as for making informed, data-driven decisions in real estate.

---

## Core Concepts and Techniques Used

This project covers key machine learning and data science techniques:

* **Linear Regression** – A statistical approach to model the relationship between a target variable and one or more input features.
* **Data Encoding** – Handling categorical variables using Label Encoding.
* **Model Training and Testing** – Splitting the dataset to evaluate model generalization.
* **Error Metrics** – Assessing model performance using MAE, MSE, and R² Score.
* **Visualization** – Plotting predicted vs actual values to understand model behavior.

---

## Data Preparation Process

Before modeling, the dataset goes through several preprocessing steps:

* **Loading the Dataset**: The data is read using `pandas` from a CSV file.
* **Categorical Variable Handling**: Features such as `mainroad`, `furnishingstatus`, and `airconditioning` are categorical and are converted into numerical format using `LabelEncoder`.
* **Data Cleaning**: The dataset is checked for missing values and inconsistencies.

---

## Feature Engineering

The dataset contains features like:

* Numeric: area, bedrooms, bathrooms, stories, parking
* Categorical (encoded): mainroad, guestroom, basement, hotwaterheating, airconditioning, prefarea, furnishingstatus

These features are combined into a feature matrix `X`, while the target variable price is stored in `y`.

---

## Model Development

The machine learning pipeline consists of the following:

1. **Splitting the Data**: Using an 80/20 split with `train_test_split()` to ensure unbiased evaluation.
2. **Model Fitting**: A `LinearRegression` model is trained using the training data (`X_train`, `y_train`).
3. **Prediction**: Once trained, the model is used to predict prices on `X_test`.

---

## Model Evaluation

To evaluate the accuracy of the model, the following metrics are computed:

* **Mean Absolute Error (MAE)**: Measures average magnitude of errors.
* **Mean Squared Error (MSE)**: Penalizes larger errors more than MAE.
* **R² Score**: Indicates how much variance in the target variable is explained by the model.

These metrics help determine how well the model performs and whether it can be trusted for future predictions.

---

## Visual Analysis

A scatter plot is generated to visualize how close the predicted house prices are to the actual prices. A red diagonal line is drawn for reference, indicating perfect prediction. The tighter the clustering around this line, the better the model performance.

---

## What Was Learned

* **Linear regression works well for interpretable modeling**, especially when relationships are mostly linear.
* **Categorical feature encoding is essential** for numerical algorithms to work effectively.
* **Evaluation metrics give a complete picture** of model accuracy and reliability.

---

## Potential Improvements

While the current model performs reasonably, there are several enhancements that could be explored:

* **Regularization**: Applying Ridge or Lasso regression to handle potential overfitting.
* **Polynomial Features**: To capture nonlinear patterns in the data.
* **Feature Scaling**: Standardizing data to improve gradient-based learning.
* **Cross-Validation**: For more robust and generalizable evaluation.

---

## How to Use This Repository

1. Clone this repository to your local machine.
2. Upload the dataset to the notebook or working directory.
3. Run the Python notebook or script line by line.
4. The output will include evaluation metrics and a price prediction plot.

---

## Dataset

The dataset used in this project can be accessed directly within the repository:
You can download the dataset used for this project here:

[Click to view/download the dataset](dataset.csv)

