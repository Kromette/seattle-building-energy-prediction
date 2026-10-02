# Seattle Building Energy Prediction

Machine learning project to predict **building energy consumption** and **CO₂ emissions** from structural and operational characteristics of non-residential buildings.

## Overview

This project uses the **2016 Seattle Building Energy Benchmarking** dataset to investigate whether energy consumption and greenhouse gas emissions can be accurately estimated from building characteristics, reducing the need for costly data collection.

The project focuses on two prediction tasks:

* Predict **total annual energy consumption**
* Predict **annual CO₂ emissions**

A particular focus is placed on **feature engineering**, **data leakage prevention**, and **rigorous model evaluation**.

## Objectives

The analysis aims to:

1. Explore and understand the structure of the dataset.
2. Identify relevant features for predicting energy consumption and CO₂ emissions.
3. Handle missing values and outliers.
4. Engineer and transform features to improve model performance.
5. Compare several regression algorithms.
6. Optimize model hyperparameters using cross-validation.
7. Evaluate the final models using appropriate regression metrics.
8. Assess the usefulness of the **ENERGY STAR Score** as a predictive feature.

## Dataset

The dataset comes from the City of Seattle's **Building Energy Benchmarking** program.

It contains information about non-residential buildings, including:

* Building size and characteristics
* Year of construction
* Building type and usage
* Energy consumption
* Greenhouse gas emissions
* ENERGY STAR Score
* Geographic and operational information

Source: [Seattle Open Data — 2016 Building Energy Benchmarking](https://data.seattle.gov/dataset/2016-Building-Energy-Benchmarking/2bpz-gwpy)

## Methodology

### 1. Exploratory Data Analysis

The first step consists of understanding the dataset and identifying:

* Missing values
* Duplicate observations
* Feature distributions
* Outliers
* Relationships between variables
* Potentially redundant or highly correlated features

Visualizations are used to investigate the main characteristics of the data and guide subsequent preprocessing decisions.

### 2. Data Cleaning

The preprocessing pipeline includes:

* Handling missing values
* Removing or treating irrelevant observations
* Identifying outliers
* Encoding categorical variables
* Transforming skewed numerical variables

Particular attention is given to avoiding **data leakage**, especially when defining the features available at prediction time.

### 3. Feature Engineering

Several transformations are investigated to extract more useful information from the raw building characteristics.

Examples include:

* Building size and structural features
* Energy-use-related ratios
* Categorical feature encoding
* Log transformations of highly skewed variables
* Normalization where appropriate

The **ENERGY STAR Score** is also evaluated to determine whether it provides meaningful additional predictive information.

### 4. Model Development

Several regression approaches are compared to establish suitable baselines and identify models capable of capturing nonlinear relationships between building characteristics and energy outcomes.

The modeling process includes:

* Baseline regression models
* Tree-based models
* Model comparison
* Cross-validation
* Hyperparameter optimization

### 5. Model Evaluation

Model performance is evaluated using regression metrics such as:

* **RMSE** — Root Mean Squared Error
* **MAE** — Mean Absolute Error
* **R²** — Coefficient of determination

Cross-validation is used during model selection and hyperparameter optimization to obtain a more robust estimate of model performance.

## Repository Structure

```text
.
├── notebooks/
│   ├── 01_exploratory_analysis.ipynb
│   ├── 02_energy_consumption_prediction.ipynb
│   └── 03_co2_emissions_prediction.ipynb
│
├── presentation/
│   └── project_presentation.pdf
│
└── README.md
```

## Technologies

* **Python**
* **Pandas**
* **NumPy**
* **Scikit-learn**
* **Matplotlib**
* **Seaborn**
* **Jupyter Notebook**

## Key Skills Demonstrated

* Exploratory Data Analysis
* Data Cleaning
* Feature Engineering
* Regression
* Machine Learning
* Cross-Validation
* Hyperparameter Optimization
* Model Evaluation
* Data Visualization
* Leakage Prevention
* Interpretable, business-oriented analysis

## Results

The project compares multiple regression approaches for both prediction tasks and identifies the best-performing models based on cross-validated performance.

The notebooks provide detailed analysis of:

* Model performance
* Feature importance
* Error analysis
* The contribution of engineered features
* The predictive value of the ENERGY STAR Score

See the notebooks for the complete analysis and results.

## Context

This project was completed as part of a **Data Scientist training program** and is based on a real-world dataset provided by the City of Seattle.

The project was designed to reproduce a realistic machine learning workflow, from exploratory analysis and feature engineering to model selection and evaluation.
