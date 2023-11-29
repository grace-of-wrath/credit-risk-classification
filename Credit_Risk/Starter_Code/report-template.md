# Module 12 Report Template

## Overview of the Analysis

The purpose of this analysis is to create a model that can predict for lenders whether a loan will be healthy or high-risk, depending on the borrower. The model was fed this existing loan data to train it: loan size,	interest rate,	borrower income,	debt to income,	number of accounts,	derogatory marks,	total debt,	and loan status (healthy or high-risk). For this analysis, I first split the data into training and test sets and then fit a logistic regression model onto the training set. I made predictions based on the model and retrieved the balanced accuracy score, confusion matrix, and classification report. I then resampled the data due to the imbalance in the loan status column (96.6% of loans in the data set were categorized as healthy) with RandomOverSampler. I repeated the process of making predictions, retrieving the balanced accuracy, confusion matrix, and classification report. 
## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

Imbalanced Logistic Regression Model:
    Balanced Accuracy: 94.4%
    Precision: 100% (0-'healthy loans'), 87% (1-'high-risk loans')
    Recall: 100% (0-'healthy loans'), 89% (1-'high-risk loans')

RandomOverSampler Logistic Regression Model:
    Balanced Accuracy: 99.4%
    Precision: 99% (0-'healthy loans'), 99% (1-'high-risk loans')
    Recall: 99% (0-'healthy loans'), 99% (1-'high-risk loans')

## Summary
The purpose of this analysis is to identify whether or not a loan would be healthy or high-risk based on the borrower.

Both models performed with high accuracy, but the OverSampler model is superior because it identifies healthy and high-risk loans with 99% accuracy, whereas the imbalanced model performed with 100% accuracy when identifying healthy loans and 87% accuracy when identifying high-risk loans. 

The increased accuracy of the OverSampler model makes it the preferable choice because it better mitigates any risk involved with lending. While the imbalanced model still performed well, in the Finance and Banking industry the difference between 87% accuracy and 99% accuracy can be stark. What's more, this difference in accuracy arises with identifying high-risk loans, meaning that the imbalanced model is more likely to misidentify a high-risk loan as a healthy one, introducing unnecessary risk to the institution.
