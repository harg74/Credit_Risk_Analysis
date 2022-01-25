# Credit_Risk_Analysis

## Overview

Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. We tested different Machine Learning techniques to train and evaluate models with unbalanced classes:

- Naive Random Sampling
- SMOTE Oversampling
- Undersampling
- SMOTEENN
- Balanced Random Forest
- AdaBoost Classifier

## Results

 | ML Model | Accuracy Score | Precision | Recall | F1 |
 | --- | --- | --- | --- | --- |
 | Naive Random Oversampling | 0.64 | 0.99 | 0.62 | 0.76 |
 | SMOTE Oversampling | 0.65 | 0.99 | 0.69 | 0.81 |
 | Cluster Centroid Undersampling | 0.54 | 0.99 | 0.40 | 0.56 | 
 | SMOTEENN Combination Sampling | 0.64 | 0.99 | 0.57 | 0.72 |
 | Balanced Random Forest Classifier | 0.79 | 0.99 | 0.87 | 0.93 |
 | Easy Ensemble AdaBoost Classifier | 0.93 | 0.99 | 0.94 | 0.97 |

Code for each one of the techniques:

- Naive Random Sampling
![image](https://user-images.githubusercontent.com/78564912/150901875-470cd071-915f-41a8-a64e-8cb454b2db28.png)

- SMOTE oversampling
![image](https://user-images.githubusercontent.com/78564912/150901931-189afae6-e4d2-475c-aa71-95276e98c41d.png)

- Undersampling
![image](https://user-images.githubusercontent.com/78564912/150902087-f1d97a7f-a68a-4c62-b5d9-403bd9358885.png)

- SMOTEENN
![image](https://user-images.githubusercontent.com/78564912/150902152-2f9f8f23-b3dc-4673-91f0-ba220e9f2e07.png)

- Balanced Random Forest
![image](https://user-images.githubusercontent.com/78564912/150901723-0ebd91a5-46ff-423d-9e16-238d50b5a696.png)

- AdaBoost Classifier
![image](https://user-images.githubusercontent.com/78564912/150901787-f3b6a2da-3111-45fb-b111-b93773fcfccf.png)

## Summary

Analyzing precision, which provide information of False Positives, for all the six algorithms had a really poor performance predicting hight risk individuals. The highest percentage we obtained was for Easy Ensemble AdaBoost Classifier with 9%, meaning that the algo mistakenly identified as high-risk individuals, low-risk individuals. Identifying only 9% of the time high-risk customers. On the other hand, all the models had a decent precision for low-risk individiuals meaning that all of the low-risk customers were marked as that.

On the other hand, the model with the highest sensitivity, which provide information about False Negatives, was the Easy Ensemble Adaboost Classifier (92% for high-risk and 94% for low-risk individuals), meaning that 92% of the time all the high-risk individuals are marked as high-risk individuals. Followed by this model, the other two with high recall were the Random Forest Classifier (70%) and SMOTEENN Resample (72%).

In the banking business, sensitivity is more valuable than precision for analyzing risk and default rates on loan candidates. This because banks want to be able to mark all of the high-risk individuals as high-risk for them not to default. It doesn't matter if it is not as precise as long as the posible defaults are marked as that. Therefore, the Easy Ensemble Adaboost Classifier (92% for high-risk and 94% for low-risk individuals), would be the algorithm selected to be applied to our future datasets to make a decision whether a customer is high or low risk to provide a credit.