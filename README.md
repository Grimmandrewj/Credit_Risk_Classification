## Goal and Analysis Overview

- The purpose of this challenge and analysis was to evaluate the efficacy of different machine learning models for assessing credit loan risk and identify the creditworthiness of borrowers.  
- The provided data consisted of historical lending activity from a peer-to-peer lending services company.  It consisted of data relating to each borrow such as loan size, interest rate, borrower income, debt to income ratio, and number of open accounts.  The goal of the analysis was to predict whether loan would be healthy or high-risk based on the borrower data.  
- The data was separated into labels and features and value counts calculated to determine the number of healthy vs. high-risk loans.

![image](https://github.com/Grimmandrewj/Credit_Risk_Classification/assets/120341249/ddaa52d8-b79f-4407-97e7-0ae164edb677)

- The following stages of machine learning were utilized throughout the process:
  - Data preparation and preprocessing - the original data was analyzed, missing           values considered, outliers identified, variables transformed as needed, the           values of the target data calculated, and the data split into training and 
    testing datasets for evaluation
    
![image](https://github.com/Grimmandrewj/Credit_Risk_Classification/assets/120341249/1a25e9ce-066e-4eb4-9061-a714b7a3a7c6)

  - Choosing a model - a logistic regression model was fit to the original                 preprocessed data (using the LogisticRegression module from SKLearn) and then to       the oversampled/resampled data (using RandomOverSampler module from Imbalanced-       Learn) in order to evaluate the results
  - Predictions - predictions were made regarding the models' performance using the       testing feature data.  These predictions were then visualized
    
![image](https://github.com/Grimmandrewj/Credit_Risk_Classification/assets/120341249/26559bf6-1124-47b7-8434-347f3cab0f99)

  - Evaluation - a confusion matrix was generated and a classification report created     for each model to document the accuracy of their predictions for both the original     and resampled data.  The Balanced_Accuracy, Confusion_Matrix, and                     Classification_Report modules were utilized for these evaluations

## Results

The results of the analysis are as follows: 

  - Model 1 (fit to original data):
    - Precision: 1.00 (healthy), 0.87 (high-risk)
    - Recall: 1.00 (healthy), 0.89 (high-risk)
    - F1 score: 1.00 (healthy), 0.88 (high-risk)

![image](https://github.com/Grimmandrewj/Credit_Risk_Classification/assets/120341249/914efaa3-d306-49ea-94f0-0305f670f74b)

  - Model 2 (fit to resampled data):
    - Precision: 1.00 (healthy), 0.87 (high-risk)
    - Recall: 1.00 (healthy), 1.00 (high-risk)
    - F1 scre: 1.00 (healthy), 0.93 (high-risk)
   
![image](https://github.com/Grimmandrewj/Credit_Risk_Classification/assets/120341249/98a0cf3f-8f3e-4419-b963-bdceeeea8992)

## Summary

The results demonstrate that both models performed well in predicting credit loan risks, with each scoring highly in each category (precition, recall, and F1).  However, Model 2 showed better performance in predicting high-risk loans as demonstrated by the higher accuracy rating.  

The specific model chosen to evaluate and predict depends greatly on the problem and the desired outcome.  A model based on resampled data appears to perform well in predicting both types of borrowers.  However, if the desire is to pinpoint and predict high-risk loans, a model with a high recall score. is preferable.  Alternatively, if the desire is to minimize inaccurate accounting of the number of potentially high-risk borrowers, then a high-precision score is preferable.  Performance of the models is highly dependent on the problem that needs to be solved and therefore will influence which model is selected. 

Overall, my recommendation would be to utilize Model 2 for this dataset as it more accurately predicts both healthy and high-risk loans across all metrics.  
