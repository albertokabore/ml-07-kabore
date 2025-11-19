# Final Project: Regression Analysis

> Submission: GitHub Repository with Jupyter Notebook and Peer Review

---

## Overview
Businesses and organizations often need to understand the relationships between different factors to make better decisions.
For example, a company may want to predict the fuel efficiency of a car based on its weight and engine size or estimate home prices based on square footage and location.
Regression analysis helps identify and quantify these relationships between numerical features, providing insights that can be used for forecasting and decision-making.

This project demonstrates your ability to apply regression modeling techniques to a real-world dataset. You will:
- Load and explore a dataset.
- Choose and justify features for predicting a target variable.
- Train a regression model and evaluate performance.
- Compare multiple regression approaches.
- Document your work in a structured Jupyter Notebook.
- Conduct a peer review of a classmate's project.

---

## Dataset Options
Select one dataset from the list below. If you get good results, you can try the process on a suitable dataset of your own. 
Suitable datasets contain **numerical features** and a **numerical target variable** for regression.

1. Auto MPG Dataset (Predict fuel efficiency based on engine specs and weight)
   - [UCI Auto MPG Dataset](https://archive-beta.ics.uci.edu/ml/datasets/auto+mpg)
2. Housing Prices Dataset (Predict home values based on features like square footage and location)   
   - [Kaggle Housing Prices](https://www.kaggle.com/c/house-prices-advanced-regression-techniques)
3. Medical Costs Dataset (Predict insurance charges based on age, BMI, smoking status)  
   - [Medical Cost Dataset](https://www.kaggle.com/mirichoi0218/insurance)

---

## Assignment Requirements
Your Jupyter Notebook must follow a structured format with clearly numbered second-level headings and reflection remarks after each section.

Start your notebook professionally with:
- a single top-level title
- your name (or alias)
- the date
- a brief introduction that describes the problem and the dataset.
- Import the external Python libraries used (e.g., pandas, numpy, matplotlib, seaborn, sklearn).

### Section 1. Import and Inspect the Data
- 1.1 Load the dataset and display the first 10 rows.
- 1.2 Check for missing values and display summary statistics.

Reflection 1: What do you notice about the dataset? Are there any data issues?

---

### Section 2. Data Exploration and Preparation
- 2.1 Explore data patterns and distributions
  - Create histograms, boxplots, and count plots for categorical variables (as applicable).
  - Identify patterns, outliers, and anomalies in feature distributions.
  - Check for class imbalance in the target variable (as applicable).
- 2.2 Handle missing values and clean data
  - Impute or drop missing values (as applicable).
  - Remove or transform outliers (as applicable).
  - Convert categorical data to numerical format using encoding (as applicable).
- 2.3 Feature selection and engineering
  - Create new features (as applicable).
  - Transform or combine existing features to improve model performance (as applicable).
  - Scale or normalize data (as applicable).

Reflection 2: What patterns or anomalies do you see? Do any features stand out? What preprocessing steps were necessary to clean and improve the data? Did you create or modify any features to improve performance?

---

### Section 3. Feature Selection and Justification
- 3.1 Choose features and target
  - Select two or more input features (numerical for regression, numerical and/or categorical for classification)
  - Select a target variable (as applicable)
    - Regression: Continuous target variable (e.g., price, temperature).
    - Classification: Categorical target variable (e.g., gender, species).
    - Clustering: No target variable.
    - Justify your selection with reasoning.
- 3.2 Define X and y
  - Assign input features to X
  - Assign target variable to y (as applicable)

Reflection 3: Why did you choose these features? How might they impact predictions or accuracy?

---

### Section 4. Train a Model (Linear Regression)
- 4.1 Split the data into training and test sets using train_test_split (or StratifiedShuffleSplit if class imbalance is an issue).
- 4.2 Train model using Scikit-Learn model.fit() method
- 4.3 Evalulate performance, for example:
  - Regression: R^2, MAE, RMSE (RMSE has been recently updated)
  - Classification: Accuracy, Precision, Recall, F1-score, Confusion Matrix
  - Clustering: Inertia, Silhouette Score

Reflection 4: How well did the model perform? Any surprises in the results?

---

### Section 5. Improve the Model or Try Alternates (Implement Pipelines)
- 5.1 Implement Pipeline 1: Imputer → StandardScaler → Linear Regression.
- 5.2 Implement Pipeline 2: Imputer → Polynomial Features (degree=3) → StandardScaler → Linear Regression.
- 5.3 Compare performance of all models across the same performance metrics

Reflection 5: Which models performed better? How does scaling impact results?

---

### Section 6. Final Thoughts & Insights
- 6.1 Summarize findings.
- 6.2 Discuss challenges faced.
- 6.3 If you had more time, what would you try next?

Reflection 6: What did you learn from this project?

---

## Tasks to Complete the Assignment

1. Create a GitHub repository named **ml_regression_yourname**.  
1. Upload your dataset to a **data folder** in the repository.  
1. Develop a Jupyter Notebook (regression_yourname.ipynb) structured as outlined above.  
1. Complete and write reflections for each section as you work.
1. Write a README.md summarizing your project, dataset, and findings (see below).
1. Review a classmate’s project and provide feedback in peer_review.md (see below).

---

## README.md (Required)

Include a professional README.md that introduces your project. Include:
- a clickable link to your notebook file.
- a clickable link to your your peer review Markdown file.
- Instructions on how to set up your virtual environment and run your notebook locally.

---

## Peer Review (Required)

Review one other GitHub repository and provide feedback on:

1. Clarity & Organization (Is the notebook structured and easy to follow?)
1. Feature Selection & Justification (Do the chosen features make sense given the objectives?)
1. Model Performance & Comparisons (Are the results and comparisons clearly explained?)
1. Reflection Quality (Are insights well thought out?)

Submission: Submit a short peer review document in your own repository titled peer_review.md.  
The peer review must contain a **clickable Markdown link to the notebook (.ipynb) file reviewed** along with your personal, well-organized and presented 4-pont review. 
Provide specifics - both positive and constructive feedback. 
Suggest improvements where possible and explain why a different choice might be useful as well.
Focus on actionable suggestions that the author could realistically implement.

---

## Repository Checklist

Verify your repository contains:

- [ ] Jupyter Notebook with proper name, numbered sections and reflections
- [ ] README.md (overview)
- [ ] PROJECT_SUMMARY.md (with modeling details - see midterm PROJECT_SUMMARY_TEMPLATE.md for front matter and questions from REGRESSION_GUIDE.md)
- [ ] Dataset, stored in a data folder
- [ ] Peer Review (peer_review.md)

