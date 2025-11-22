# Project Summary – Medical Insurance Cost Regression  
**Author:** Albert Kabore  
**Date:** November 22, 2024  

## Project Purpose  
This project uses regression modeling to predict individual medical insurance charges based on demographic and health-related variables. The goal is to identify key drivers of insurance cost — such as age, BMI, smoking status, and interactions between features — and build models that can reasonably estimate insurance charges from input features. This can help insurance providers understand risk factors and set premiums more systematically.  

## Dataset  
- **Source file:** `data/insurance.csv`  
- **Description:** The dataset contains 1,338 records. Each record includes:  
  - Numeric features: `age`, `bmi`, `children`  
  - Categorical features: `sex`, `smoker`, `region`  
  - Target variable: `charges` (annual insurance cost)  
- No missing values — dataset is clean.  

## Data Processing & Feature Engineering  
- One-hot encoding of categorical variables (`sex`, `smoker`, `region`)  
- Engineered new features to capture potential nonlinear and interaction effects:  
  - `age_squared` (age²)  
  - `bmi_age_interaction` (BMI × age)  
  - Binary flags: `is_overweight` (BMI > 25), `has_children` (children > 0)  
- Final selected features for modeling: `age`, `bmi`, `children`, `smoker_yes`, `age_squared`, `bmi_age_interaction`  

## Modeling Approach  
Three regression approaches were implemented and compared:

| Model | Preprocessing & Model Pipeline |
|-------|-------------------------------|
| **Baseline Linear Regression** | Direct fit on selected features |
| **Pipeline 1** | Median imputation → Standard scaler → Linear regression (same features) |
| **Pipeline 2** | Median imputation → Polynomial features (degree = 2) → Standard scaler → Linear regression |

Evaluation metrics: R² (coefficient of determination), MAE (mean absolute error), RMSE (root mean squared error).

## Results (Test Set Performance)  

| Model | R² | MAE (USD) | RMSE (USD) |
|-------|-----|-----------|-------------|
| Baseline Linear Regression | ~0.782 | ~4,138 | ~5,815 |
| Pipeline 1 (Scaled Linear) | ~0.782 | ~4,138 | ~5,815 |
| Pipeline 2 (Polynomial) | ~0.869 | ~2,768 | ~4,512 |

The polynomial regression model substantially outperformed the linear models, explaining ≈ 87% of the variance in insurance charges, and reducing average error by more than \$1,300 versus baseline.

## Key Findings & Insights  

1. **Smoking status** is the strongest predictor of insurance charges.  
2. There is a **nonlinear relationship** between age and charges — older age, especially when combined with other factors (e.g., BMI), increases cost nonlinearly.  
3. Polynomial regression with interaction and squared terms significantly improves predictive performance.  
4. Even with a relatively simple model (degree-2 polynomial + linear regression), the model achieves good generalization with RMSE around \$4,500 and MAE around \$2,770.  

## Limitations & Challenges  
- The `charges` variable is right-skewed — large values exist and could dominate error metrics.  
- Polynomial features increase model complexity and may risk overfitting.  
- No cross-validation was implemented (only a single train/test split), limiting robustness.  
- Model assumes relationships are (polynomial) linear; other algorithms (tree-based, ensemble, regularized models) might capture more complex patterns.  

## Future Work & Improvements  

If given more time, I would:  
- Apply **cross-validation** to better estimate generalization performance.  
- Explore **regularization** (e.g., Ridge, Lasso) to reduce overfitting risk from polynomial terms.  
- Test **non-linear algorithms** (e.g., Random Forest, Gradient Boosting, Neural Networks).  
- Transform the target variable (`charges`) — e.g., log-transform — to handle skewness.  
- Conduct **feature selection/importance analysis** to reduce dimensionality and improve interpretability.  
- Evaluate model stability and fairness across subgroups (e.g., smokers vs non-smokers, BMI ranges, age groups).  

## Conclusion  

This project demonstrates that, with thoughtful feature engineering and polynomial terms, a regression model can predict medical insurance costs reasonably well. The strong influence of smoking status and the nonlinear effects of age highlight how health and behavior variables play a critical role. The polynomial model’s improved performance shows that capturing interactions and non-linearity adds significant predictive power.  

With further enhancements (regularization, cross-validation, more advanced models), the predictive model can become both more accurate and more robust — making it more useful for real-world insurance pricing or risk assessment.

