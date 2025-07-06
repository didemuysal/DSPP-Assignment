# E.coli-Protein-Localization-Prediction

## Overview
This project predicts the localization site of proteins in E. coli bacteria using the ecoli.csv dataset. The goal is to classify proteins as either belonging to the cell membrane or the periplasm. Two machine learning models, Gaussian Naive Bayes and Logistic Regression, are implemented and evaluated to solve this binary classification problem. The analysis includes data preprocessing, feature scaling, model training, and performance comparison.


## Data Preprocessing
Initial exploratory data analysis including:
- Checking for missing values: The dataset is confirmed to be complete with no missing values.
- Identifying numerical variables: All features in the dataset are numerical, which simplifies the preprocessing steps.
- Feature Scaling

To ensure that all features contribute equally to the model's performance, the feature matrix X is scaled using the scale function from scikit-learn. This standardizes the features to have a mean of 0 and a standard deviation of 1.

## Model Implementation
The dataset is split into training and testing sets, with 80% of the data used for training and 20% for testing. Two models are then implemented:
* Gaussian Naive Bayes: A GaussianNB classifier is trained on the scaled training data.

* Logistic Regression: A LogisticRegression classifier is also trained on the same data.

## Results
Both models were evaluated on their predictive performance. The Logistic Regression model showed better results across most metrics on the raw test data.

| Metric               | Gaussian Naive Bayes   | Logistic Regression   |
|----------------------|------------------------|-----------------------|
| Accuracy             | 0.62                   | 0.69                  |
| Precision            | 0.60                   | 0.71                  |
| Recall               | 0.27                   | 0.45                  |
| F1 Score             | 0.37                   | 0.56                  |
| ROC AUC              | 0.55                   | 0.64                  |

While Logistic Regression performed better initially, cross-validation suggested that the Gaussian Naive Bayes model was more robust and less prone to underfitting with each fold.



