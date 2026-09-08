# Medical Insurance Cost Analysis

Exploratory data analysis and regression modelling of medical insurance charges using Python, Pandas and scikit-learn.

## Project objective

The goal of this project is to analyse the variables associated with annual medical insurance charges and build regression models capable of estimating `charges` from demographic and lifestyle-related features.

The dataset contains 2,772 observations and the following variables:

- Age
- Gender
- BMI
- Number of children
- Smoking status
- Region
- Annual insurance charges

## Analysis workflow

### 1. Data loading and cleaning

The raw dataset is imported into a Pandas DataFrame, column names are assigned, missing values are identified, and incomplete observations are handled according to variable type.

### 2. Exploratory data analysis

Relationships between insurance charges and the available predictors are explored using:

- Regression plots
- Box plots
- Correlation analysis
- Descriptive statistics

Smoking status shows the strongest linear association with insurance charges in this dataset.

### 3. Baseline regression models

Several regression approaches are evaluated:

- Single-variable linear regression
- Multivariable linear regression
- Polynomial feature transformation
- Ridge regression

### 4. Train/test evaluation

The data is split into training and testing subsets, reserving 20% of observations for held-out evaluation.

A Ridge regression model is then evaluated before and after applying second-degree polynomial feature expansion.

## Results

Key model results from the notebook:

| Model | Evaluation | R² |
|---|---|---:|
| Linear regression using smoking status | Full dataset | 0.622 |
| Multivariable linear regression | Full dataset | 0.750 |
| Polynomial linear-regression pipeline | Full dataset | 0.845 |
| Ridge regression | Test set | 0.676 |
| Polynomial features + Ridge regression | Test set | **0.784** |

The most relevant performance estimate is the held-out test result. The polynomial Ridge model explains approximately **78% of the variance in insurance charges on the test subset** in this analysis.

> The higher 0.845 value is an in-sample score and should not be interpreted as held-out predictive performance.

## Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- scikit-learn
- Jupyter Notebook

## Repository contents

- `Data.A-Project1.ipynb` — complete analysis and modelling workflow

## Data source

The project uses the medical insurance dataset supplied through the IBM Skills Network learning environment.

## Notes

This project was originally developed as a practice data-analysis exercise and has been retained as a compact example of an end-to-end tabular regression workflow.

## Project type

**Exploratory Data Analysis · Regression · Machine Learning**
