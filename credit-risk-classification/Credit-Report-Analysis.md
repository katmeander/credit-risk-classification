# Module 12 Report Template

## Overview of the Analysis

Purpose
It is important to be able to assess the creditworthiness of borrowers so a lender can predict which information is important to gather about a borrower for determining whether they should choose to give them a loan. 

For this analysis, I looked at historical lending activity that included the following information about borrowers:

	•	Loan Size
	•	Interest Rate
	•	Borrower Income
	•	Debt to Income ratio
	•	Number of accounts
	•	Derogatory marks on credit report
	•	Total Debt
	•	Whether their loan was considered “Healthy” or “At-Risk”

For this analysis I was attempting to predict whether a potential loan should be classified as healthy or at-risk using the "Loan Status" (health or at-risk) information in the dataset.

For this process I took a sample of the data, the loan size, interest rate of loan, income, debt, number of accounts, derogatory marks, and total debt and ran them through the model to see how often it could correctly predicted if those features determined a healthy or at-risk loan.
After training the model I took the remaining data not in the sample and used that to test the model. 

I used the LogisticRegression module to model, fit and predict the accuracy, confusion matrix and classification report.
I then resampled the data with the RandomOverSampler module and ran the resampled data again through the LogisticRegression model, generating accuracy, confusion matrix and a classification report.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  	•	Accuracy: 0.944 or 94.4% accuracy

	•	Precision: 
	⁃	Healthy loan: 1.00 or 100%
	⁃	At-risk loan: 0.87 or 87%

	•	Recall: 
	⁃	Healthy loan: 1.00 or 100%
	⁃	At-risk loan: 0.89 or 89%


* Machine Learning Model 2:
 	•	Accuracy: 0.99.45 or 99.45% accuracy

	•	Precision:
	⁃	Healthy loan: 0.99 or 99%
	⁃	At-risk loan: 0.99 or 99%

	•	Recall:
	⁃	Healthy loan: 0.99 or 99%
	⁃	At-risk loan: 0.99 or 99%


## Summary

While the first model has higher precision and recall scores at predicting healthy loans at 100%, the risk is in the prediction power of the at-risk loans where the precision and recall scores are quite low at 87% and 89%, respectively. For this reason I do not recommend the first model. Rather, I recommend the second model, with just a 1% drop in precision and recall for healthy loans compared to the first model, it has a higher accuracy rate overall and a much higher precision and recall prediction rate for at-risk loans, where the risk is the highest.
