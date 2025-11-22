# ml-07

## Regression Analysis Project – Medical Insurance Costs

#### Author: Albert Kabore
#### Date: November 22, 2024

## Project Overview
This project demonstrates a comprehensive regression analysis to predict individual medical insurance charges based on demographic and health-related factors. Using machine learning techniques, we analyze how age, BMI, smoking status, and other features influence insurance costs, providing insights that could help insurance companies with risk assessment and premium pricing.

**Dataset**: Medical Insurance Costs (1,338 records, 7 features)
**Target Variable**: Insurance charges (continuous)
**Problem Type**: Regression Analysis

## Key Findings
- **Best Model**: Polynomial Regression (Degree=2) achieved R² = 0.87
- **Strongest Predictor**: Smoking status (correlation: 0.79)
- **Key Insights**: Age shows non-linear relationship with charges, BMI-age interactions are significant
- **Average Prediction Error**: $3,152


## Quick Links
- [**Jupyter Notebook**](regression_analysis.ipynb) - Complete analysis with code and insights
- [**Peer Review**](peer_review.md) - Feedback on classmate's project
- [**Project Summary**](PROJECT_SUMMARY.md) - Detailed modeling methodology and results

## Models Implemented
1. **Simple Linear Regression** (Baseline)
2. **Pipeline 1**: StandardScaler + Linear Regression
3. **Pipeline 2**: Polynomial Features + StandardScaler + Linear Regression

## Performance Comparison
| Model | R² Score | MAE | RMSE |
|-------|----------|-----|------|
| Simple Linear Regression | 0.76 | $4,152 | $6,098 |
| Scaled Linear Regression | 0.76 | $4,152 | $6,098 |
| Polynomial Regression | **0.87** | **$3,152** | **$4,782** |

## Features Used
- **Demographic**: age, children
- **Health**: bmi, smoker_yes
- **Engineered**: age_squared, bmi_age_interaction

## Setup Instructions

### Prerequisites
- Python 3.7+
- Jupyter Notebook
- Required Python packages

### Installation

1. **Clone the repository**
```Powershell
git clone https://github.com/albertokabore/ml-07-kabore
```


Create virtual environment

```Powershell
python -m venv insurance_env
```
source insurance_env/bin/activate  # On Windows: insurance_env\Scripts\activate

#### Install dependencies

```Powershell
pip install -r requirements.txt
``

```Powershell
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
Launch Jupyter Notebook
```

```Powershell
jupyter notebook
```
- Navigate to regression_analysis.ipynb

- Run cells sequentially to reproduce the analysis

#### Dependencies
```Powershell
pandas >= 1.3.0

numpy >= 1.21.0

matplotlib >= 3.4.0

seaborn >= 0.11.0

scikit-learn >= 1.0.0

jupyter >= 1.0.0
```
## Project Structure

#### Section 1

Importing libraries, loading the dataset, inspection of variables, datatypes, and missing values.

#### Section 2

Exploration of patterns through descriptive statistics, visualizations, and outlier inspection.

Data preparation includes encoding of categorical variables and creation of engineered features.

#### Section 3

Selection and justification of features used to build predictive models.

Definition of the input matrix X and target vector y.

#### Section 4

Training and evaluation of a linear regression model.

Assessment using R², MAE, and RMSE.

#### Section 5

- Implementation of advanced regression models using Scikit-Learn pipelines.
- Pipeline 1 uses an imputer, scaling, and linear regression.
- Pipeline 2 introduces polynomial features, scaling, and linear regression.
- Performance of all models is compared using a summary table and visual plots.

#### Section 6

- Final insights, challenges, and potential improvements.

