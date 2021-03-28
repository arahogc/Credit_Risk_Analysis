# Credit_Risk_Analysis

## Overview 

The purpose of this project is to use supervised machine learning to help determine which customers are "low" or "high" risk for loan applications. There were six machine learning models that are in two camps of analysis-resampling and ensemble. For resampling, the following models were used: Naive Random Oversampling, SMOTE Oversampling, Undersampling with Cluster Centroids, and a combination of over- and undersampling with SMOTEEN. For ensemble, two models were used: Balanced Random Forest Classifier and an Easy Ensemble AdaBoost classifier. For all machine learning models, we will be comparing the balanced accuracy score, the precision and recall scores to see which, if any, are the best techniques to determine if a customer is high or low risk for loans. For all analysis, the string values in the csv file was converted into numbers using get_dummies to make it easier for machine learning. 

## Results 

### Naive Random Oversampling 

* Balanced Accuracy Score: 65.5%
* Precision Score 
    * High Risk: 64%
    * Low Risk: 67%
    * Average: 66%
* Recall Score
    * High Risk: 69%
    * Low Risk: 62% 
    * Average: 65%

### SMOTE Oversampling 

* Balanced Accuracy Score: 64.8%
* Precision Score 
    * High Risk: 66%
    * Low Risk: 64%
    * Average: 65%
* Recall Score
    * High Risk: 60%
    * Low Risk: 69% 
    * Average: 65%

### Cluster Centroids (undersamping) 

* Balanced Accuracy Score: 66.7%
* Precision Score 
    * High Risk: 69%
    * Low Risk: 65%
    * Average: 67%
* Recall Score
    * High Risk: 60%
    * Low Risk: 73% 
    * Average: 67%

### SMOTEENN (Combination Sampling)

* Balanced Accuracy Score: 66.1%
* Precision Score 
    * High Risk: 66%
    * Low Risk: 68%
    * Average: 67%
* Recall Score
    * High Risk: 76%
    * Low Risk: 56% 
    * Average: 67%

### Balanced Random Forest Classifier

* Balanced Accuracy Score: 78.9%%
* Precision Score 
    * High Risk: 3%
    * Low Risk: 100%
    * Average: 99%
* Recall Score
    * High Risk: 70%
    * Low Risk: 87% 
    * Average: 87%

### Easy Ensemble AdaBoost Classifier

* Balanced Accuracy Score: 69.4%
* Precision Score 
    * High Risk: 77%
    * Low Risk: 66%
    * Average: 67%
* Recall Score
    * High Risk: 86%
    * Low Risk: 45% 
    * Average: 69%

## Summary 

When assessing which machine learning models are "good" it is important to look at not only the precision score (ratio of correctly predicted positive observations to the total predicted positive observations) but also the recall score. The recall score, which is ratio of correctly predicted positive observations to all observations in the observed class, is considered "good" when it is above 0.5. Of course, with a precision score, the higher the score, the better. 

Overall, it appears that the one model we should avoid for assessing low risk loan applications would be the Easy Ensemble AdaBoost Classifier, since it has a low recall score for the low risk category. Meanwhile the best for low risk assessment would be the Balanced Random Forest Classifier- with a precision score of 100% and the recall score of 87%. It also has a high accuracy score (~79%). 

For high risk applications, it appears that the Easy Ensemble AdaBoost Classifier is the best, especially with it is high accuracy score (~70%). The worst for high risk applications would be the Balanced Random Fores Classifier since it's precision score for high risk is at 3%. However, it is not very convenient to use two different models for assessing loan applications. So the other models are good enough for assessement, since they all have similar accuracy, recall, and precision scores, but not as great as the EEAC or BRFC. It is recommended to keep looking for a model that can accurately predict all categories, but continue to use the EEAC and BRFC to predict high and low risk loan applications. 


