# Credit Risk Analysis
---
## Overview of the Analysis: 
---
Using credit application data to predict if the applicant is high or low risk using a 
variety of machine learning algorithms.
The Machine Learning algorithms use   

## Results: 
---
Precision: is the proportion of the positive identification that was actually correct. 
Precision = TruePositives / (TruePositives + FalsePositives) 

Recall: is the proportion of the actual positives that were identified correctly.
Recall - TruePositives / (TruePositives + FalseNegatives)

Accuracy is also used to evaluate a classification model.  Is a fraction of the model 
that were predicted correctly.
Accuracy = TotalCorrect / TotalNumberPredictions

Because the data for credit application is not balanced, meaning there are for more 
application that are lower risk than higher risk, several sampling tools were used 
to sample the data before using the logistic Regression to predict if an applicant 
was high or low risk.  Logistic Regression is used to predict a TRUE or FALSE 
Positive or Negative result.   

### Random Over Sampler
The accuracy = 0.637
The precision of this model for high risk is 0.01 however it was 100% at getting the 
correct low risk applicants

![Random Over Sampler](/images/bac_RandomOverSampler.png)

### SMOTE Oversampling
The Accuracy = 630
Similar results as the Random Over Sampler

![SMOTE](/images/smote.png)

### Cluster Centroids
Clusters Centroids is a classification to under sample the data. instead of creating 
additional similar data points, it removes samples from the large group to balance 
the data sets between high and low risk.  This helps reduce bias in the results

Accuracy = 0.529
The accuracy score is lower than the other samples, but the recall of this classification 
is much lower

![Clusters Centroids](/images/cc.png)

### Combination Sampling
Accuracy = 0.638
The recall percentages are a little better than Cluster Centroids and the accuracy is 11% better,

![SMOTTENN](/images/smottenn.png)

## The next two are Ensemble Learners algorithms
---
### Balanced Random Forest Classifier
Accuracy = .795
Using this ML algorithms has a much higher accuracy and now seeing that recall are better 
than the other results.  This predicted fewer false negatives.

![Balanced Random Forest Classifier](/images/brfc.png)

### Easy Ensemble AdaBoost Classifier
Accuracy = 0.920
This algorithms produce the best results with the highest accuracy and 

![Easy Ensemble AdaBoost Classifier](/images/eeac.png)

## Summary: 
---
A variety of sampling techniques were used however those did not produce quality results
as the last algorithm used.  Easy Ensemble AdaBoost Classifier had the highest 
accuracy score and the precision and recall relationships were better aligned to predict 
those applicant with high risk of defaulting on their credit.

