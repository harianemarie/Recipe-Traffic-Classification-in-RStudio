# Recipe Traffic Classification


## Project Overview

This project focuses on predicting whether a recipe published on a cooking website is likely to generate **high website traffic**.

The dataset contains information about recipes, including their nutritional characteristics, recipe category, number of servings, and traffic level. The objective is to identify the factors associated with high traffic and build predictive models capable of classifying recipes according to their expected traffic level.

---

## 🎯 Objectives

The main objectives of this project were to:

* Clean and prepare the dataset
* Handle missing values and data inconsistencies
* Perform exploratory data analysis (EDA)
* Identify relationships between recipe characteristics and website traffic
* Build and compare several classification models
* Evaluate model performance using appropriate metrics
* Identify the variables most associated with high traffic

---

## 📊 Dataset

The raw dataset contains **947 observations** and information related to:

* Recipe identifier
* Calories
* Carbohydrates
* Sugar
* Protein
* Recipe category
* Number of servings
* Website traffic level (`high_traffic`)

The target variable is **`high_traffic`**, which indicates whether a recipe is associated with high website traffic.

---

## 🔎 Data Preparation

The project includes several preprocessing steps:

* Data quality and consistency checks
* Duplicate detection
* Missing-value analysis
* Handling of missing observations
* Variable transformation
* Conversion of categorical variables into factors
* Creation of a numerical version of the target variable
* Exploratory analysis of the target distribution
* Train/test dataset splitting

The final dataset was then used to train and evaluate the predictive models.

---

## 📈 Exploratory Data Analysis

Several visualizations and statistical analyses were performed to investigate the relationship between recipe characteristics and traffic.

The analysis explored:

* Traffic distribution
* Recipe categories and traffic levels
* Number of servings
* Calories
* Protein
* Carbohydrates
* Sugar
* Outliers and transformed variables

The project also examined how nutritional characteristics and recipe categories were associated with high or low website traffic.

---

## Machine Learning Models

Three classification approaches were implemented and compared:

### 1. Linear Probability Model (LPM)

A Linear Probability Model was used as a baseline classification approach to estimate the probability of a recipe generating high traffic.

### 2. Logistic Regression

A Logistic Regression model was developed to estimate the probability that a recipe belongs to the **high-traffic** class and to identify the variables associated with this outcome.

### 3. Random Forest

A Random Forest model was implemented to capture potentially non-linear relationships between recipe characteristics and website traffic.

The model was optimized using **10-fold cross-validation**, with the number of variables randomly selected at each tree split (`mtry`) evaluated using accuracy and AUC.

---

## 📏 Model Evaluation

The models were evaluated using:

* Accuracy
* Sensitivity / Recall
* Specificity
* Confusion Matrix
* ROC Curves
* Area Under the Curve (AUC)

The Random Forest model used **500 trees**, with an optimal `mtry` value of **2** based on the cross-validation results.

---

## Key Findings

The analysis highlights the importance of **recipe category** in explaining high website traffic.

The Random Forest variable-importance analysis identified `category` as the most associated variable with high traffic, followed by:

1. `protein`
2. `calories`
3. `sugar`
4. `carbohydrate`
5. `servings`

The analysis also investigated which recipe categories were associated with higher traffic levels.

---

## Business Perspective

Beyond model development, the project considers how predictive analysis could support the cooking website's business objective: increasing traffic and, ultimately, the probability of subscription sales.

Potential applications include:

* Promoting recipe categories associated with higher traffic
* Personalizing recipe recommendations
* Improving user engagement through ratings and reviews
* Analyzing user behavior such as clicks and time spent on pages
* Improving the visual presentation of recipes

---

## Skills Demonstrated

**Data Analysis**

* Data cleaning
* Exploratory Data Analysis
* Data visualization
* Missing-value analysis
* Outlier analysis

**Machine Learning**

* Classification
* Logistic Regression
* Linear Probability Model
* Random Forest
* Cross-validation
* Model comparison

**Model Evaluation**

* Confusion matrices
* ROC curves
* AUC
* Accuracy
* Sensitivity
* Specificity

**Tools & Technologies**

* R
* RStudio
* tidyverse
* ggplot2
* caret
* ranger
* pROC
* yardstick

---

## Project Structure

```text
recipe-traffic-classification/
│
├── data/
│   └── raw/
│       └── recipe_site_traffic_2212.csv
│
├── scripts/
│   └── classification.R
│
├── README.md
└── report/
    └── classification_report.html
```

---

## 👥 Team

* **Hariane TOGNIBO**
* **Bintou Daouda GARANGO**
* **N'gagnin Jean Luc OTODJI**

---

## 📚 Academic Context

This project was completed as part of the **Classification, Prediction & Regression** course using **RStudio**.
