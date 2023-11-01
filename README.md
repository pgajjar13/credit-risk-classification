# credit-risk-classification
Module 20 challenge

Machine learning techniques were employed to analyze a dataset comprising historical lending activity from a peer-to-peer lending services company. The goal was to construct a model capable of assessing the creditworthiness of borrowers.

**Analysis Overview:**

In this analysis, various factors were taken into account, including:

- Loan size
- Interest rate
- Borrower's income
- Debt-to-income ratio
- Number of borrower-held accounts
- Derogatory marks against the borrower
- Total debt

The dataset, consisting of 77,536 data points, was divided into training and testing sets. The training set was used to create an initial logistic regression model (Logistic Regression Model 1) with the LogisticRegression module from scikit-learn. This model was then applied to the testing dataset to determine whether a loan to a borrower would be categorized as low- or high-risk, and the results are summarized below.

The initial model was trained on a dataset containing 75,036 low-risk loan data points and 2,500 high-risk data points. To ensure that the logistic regression model had an equal number of data points for both low-risk (0) and high-risk (1) loans, the training set data was resampled using the RandomOverSampler module from imbalanced-learn. This resampling resulted in 56,277 data points for each category, based on the original dataset.

The resampled data was then used to build a new logistic regression model (Logistic Regression Model 2), with the same purpose as Model 1. The results of Model 2 are also summarized below.

**Results:**

**Logistic Regression Model 1:**

- Precision: 93% (on average, with 100% precision in predicting low-risk loans and 87% precision in predicting high-risk loans)
- Accuracy: 94%
- Recall: 95% (on average, with 100% recall in predicting low-risk loans and 89% recall in predicting high-risk loans)

**Logistic Regression Model 2:**

- Precision: 93% (on average, with 100% precision in predicting low-risk loans and 87% precision in predicting high-risk loans)
- Accuracy: 100%
- Recall: 100%

**Summary:**

Logistic Regression Model 2 demonstrates a reduced likelihood of producing false negative results. However, based on the confusion matrices for each model, Logistic Regression Model 2 predicts slightly more false positives, categorizing loans as low-risk when they are, in fact, high-risk.

If the primary objective of the model is to assess the likelihood of high-risk loans, it's important to note that neither model achieves a precision score above 90%. Nevertheless, Logistic Regression Model 2 outperforms Model 1 in terms of overall accuracy and recall and would be the preferred model due to its higher accuracy and recall, despite the slightly increased false positive rate.