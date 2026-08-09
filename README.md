# Heart Disease Prediction

 A machine learning classification project for predicting the presence of heart disease using patient health and clinical features.

---

## Project Overview

Heart disease is influenced by several clinical and demographic factors. Machine learning can be used to analyze these factors and identify patterns associated with the presence of heart disease.

This project develops and compares multiple supervised machine learning classification algorithms to predict whether a patient is likely to have heart disease.

---

## Business Objective

Build a machine learning model that can predict the potential presence of heart disease based on patient health-related features.

The project also aims to:

* Explore the relationships between clinical features and heart disease
* Prepare and preprocess the data
* Compare different classification algorithms
* Tune selected models
* Identify the best-performing model using evaluation metrics

---

## Dataset

The dataset combines patient information from two files:

* `heart disease.csv`
* `label_data.csv`

The two datasets are merged using `patient_id`.

### Target Variable

`heart_disease_present`

The target indicates whether heart disease is present.

---

## Features

The project uses clinical and demographic features including:

* Age
* Sex
* Chest pain type
* Resting blood pressure
* Serum cholesterol
* Fasting blood sugar
* Resting ECG results
* Maximum heart rate achieved
* Exercise-related ST segment slope
* ST depression
* Number of major vessels
* Thalassemia result

---

## Exploratory Data Analysis

The project performs both univariate and multivariate analysis to understand the dataset.

### Analysis includes:

* Distribution analysis
* Histograms
* Count plots
* Scatter plots
* Pair plots
* Correlation analysis
* Heatmap visualization
* Outlier analysis

The analysis is used to understand the relationships between patient characteristics and heart disease.

---

## Data Preprocessing

The preprocessing workflow includes:

* Checking dataset structure
* Checking missing values
* Checking duplicate records
* Converting categorical variables into numerical values
* Removing the `patient_id` column
* Detecting outliers
* Handling identified outliers
* Correlation analysis
* Feature scaling

`thal` was manually encoded into numerical categories, and selected numerical variables were scaled using **MinMaxScaler**.

---

## Machine Learning Models

Multiple classification algorithms were developed and evaluated:

| Model                  | Type                          |
| ---------------------- | ----------------------------- |
| Logistic Regression    | Linear Classification         |
| Support Vector Machine | Classification                |
| Naive Bayes            | Probabilistic Classification  |
| XGBoost                | Ensemble Learning             |
| Decision Tree          | Tree-based Classification     |
| Random Forest          | Ensemble Learning             |
| K-Nearest Neighbors    | Distance-based Classification |

---

## Hyperparameter Tuning

Hyperparameter optimization was performed for:

### Decision Tree

`GridSearchCV` was used to search for suitable combinations of:

* Criterion
* Maximum depth
* Minimum samples split
* Minimum samples leaf
* Splitter

### Random Forest

`RandomizedSearchCV` was used to optimize parameters including:

* Number of estimators
* Maximum features
* Maximum depth
* Minimum samples split
* Minimum samples leaf
* Bootstrap

---

## Model Evaluation

The models were evaluated using:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix
* Classification Report

This allows the models to be compared from multiple performance perspectives rather than relying only on accuracy.

---

## Best Performing Model

After comparing the classification models, the **Decision Tree classifier** achieved the best overall performance in the project.

| Metric   |      Score |
| -------- | ---------: |
| Accuracy | **93.55%** |
| F1-score |   **0.92** |

The project conclusion identifies the Decision Tree model as the best-performing model based on accuracy and F1-score.

---

## Key Takeaways

* Clinical and demographic variables can be used to identify patterns associated with heart disease.
* Multiple classification algorithms were compared.
* Hyperparameter tuning was applied to Decision Tree and Random Forest models.
* Model performance was assessed using several classification metrics.
* The tuned model comparison helped identify the strongest-performing approach.

---

## Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Seaborn**
* **Scikit-learn**
* **XGBoost**
* **SciPy**
* **Sweetviz**
* **Jupyter Notebook**

