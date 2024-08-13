# STATS202FinalProject

## Overview
This project focuses on developing predictive models to determine the relevance of URLs for search engine queries. Using a real-world dataset that includes various signals, the goal was to analyze these features and build effective models that accurately predict whether a URL is relevant to a given search query.

The dataset consists of 80,046 observations in the training set and 30,001 observations in the test set. The training data includes 10 different features (or signals) that might influence URL relevance, alongside a target variable indicating relevance (1 for relevant, 0 for not relevant). The challenge was to use this data to build models that can predict the relevance of URLs in the test set, which lacks the target variable.

## Project Steps
1. **Data Exploration and Preprocessing:**
   - Performed an initial exploration of the dataset to understand the distribution of relevant and non-relevant URLs.
   - Checked for missing values and confirmed that the dataset was clean and ready for modeling.

2. **Outlier Detection and Handling:**
   - Used Z-score analysis to identify outliers in the dataset.
   - Applied a capping transformation to limit the influence of extreme values, preserving data structure while mitigating the impact of outliers.

3. **Feature Engineering:**
   - Used box plots to visualize the relationships between features and the target variable, identifying the most predictive attributes.
   - Analyzed feature correlations using a heatmap correlation matrix, removing redundant features and adding interaction terms to capture non-linear relationships.
   - Applied K-Means clustering to create a new feature based on cluster labels, which helped capture underlying patterns in the data.

4. **Model Selection and Evaluation:**
   - Explored multiple classification models, including logistic regression, Linear Discriminant Analysis (LDA), a neural network MLP classifier, and a gradient boosting classifier.
   - Used 5-fold cross-validation to evaluate model performance, balancing the bias-variance tradeoff and ensuring the models generalize well to unseen data.
   - Fine-tuned the hyperparameters of the gradient boosting model, which emerged as the best-performing model in terms of accuracy.

## Results
The gradient boosting classifier achieved the highest accuracy among the models tested, with an average cross-validation score of 0.667. This model was selected as the final model for predicting URL relevance in the test dataset.

## Conclusion
This project successfully developed a robust model for predicting URL relevance, demonstrating the effectiveness of feature engineering, outlier handling, and careful model tuning. The methods and models used in this project can be applied to similar predictive modeling tasks, especially those involving classification problems with real-world data.
