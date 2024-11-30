## Overview of the Analysis

The purpose of this analysis was to evaluate and train a model based on loan risk using various techniques that will identify the credit worthiness of borrowers. The dataset used for this analysis consisted of 77,536 data points. The data included loan size, interest rate, borrower income, debt-to-income ratio, number of accounts, derogatory marks, and total debt. All used to determine if there is a risk associated with a loan. The goal was to predict the loan status, either as a healthy loan (0) or high-risk loan (1).

The programming for this analysis was performed in Jupyter Notebook and the steps of the machine learning process in this analysis included:
1.	Splitting the data into training and testing datasets
    - Read the .csv file into a Pandas DataFrame
    - Separate the data into labels and features; labels set (y) and features (X)
    - Import the train_test_learn module from SKLearn and split the data and assign a random_state of 1 to the function.
	

2. Creating logistic regression model with the original data
    - Import the LogisticRegression module from SKLearn, instantiate the LogisticRegression model, assign a random_state parameter of 1 to the model, then fit the model using the training data.
    - Make a prediction using the testing data; save the predictions on the testing data labels by using the testing feature data (X_test) and the fitted model

3.	Evaluating the model's performance using accuracy, precision, and recall scores
    - Generate a confusion matrix for the model
    - Print the classification report.
 

## Results

Results
The accuracy scores and the precision and recall scores of all machine learning model is as follows:

The overall accuracy of the machine learning model was 99%

    ~ Healthy loans (0): The model has a precision of 100%, which means it's excellent at identifying true positives with very few false positives. 

    ~ High-risk loans (1): The model has a precision of 84%, indicating its moderate effectiveness in identifying high-risk loans with some false positives.

    ~ Healthy loans (0): The model has a recall of 99%, which means it's correctly identifying nearly all instances of healthy loans with very few false negatives.

    ~ High-risk loans (1): The model has a recall of 94%, indicating its effectiveness in identifying high-risk loans with some false negatives.


## Summary

Based on the results, the trained logistic regression model performed well, particularly in healthy loan precision and recall. High-risk loans performed lower precision and recall. Lower precision and recall scores for high-risk loans would need to be higher because it is crucial in minimizing potential financial losses for the lending company.

I recommend resampling the data using the logistic regression model for credit risk analysis. It will show a significant improvement in predicting high-risk loans compared to the original model. The updated model will help the company effectively assess loan applications and make informed decisions when approving or rejecting loans, thus mitigating credit risk.
