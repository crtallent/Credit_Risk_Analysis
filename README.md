# Credit_Risk_Analysis

## Overview

For this project, we are tasked with applying machine learning methods to determine which model is superior when predicting credit card risk. Since the number of low-risk loans issued are much higher than those that are high-risk, the datasets will be imbalanced. This requires us to use a variety of methods and techniques to train and evaluate models with unbalanced classes (datasets in which values are heavily slanted). For this project, the imbalanced-learn and skikit-learn libaries were used as they have unbalanced classes in their models. 

The data being evaluated is a [credit card dataset](https://github.com/crtallent/Credit_Risk_Analysis/tree/main/Resources) from Lending Club, which is a peer-to-peer lending services company. In order to complete our analyses of the dataset, we used multiple algorithms from the above-mentioned libraries. We then evaluated the performance of by performing logistic regression and then calculating the accuracy, precision, and sensitivity of each algorithm:

* Oversampling with RandomOverSampler and SMOTE
* Undersampling with ClusterCentroids
* Combination approach (oversampling and undersampling) with SMOTEENN
* Bias-reducing models with BalancedRandomForestClassifer and EasyEnsembleClassifer

## Resources

* Software: Python 3.7.6, Jupyter Notebook 7.29.0
* Data Source: [LoanStats_2019Q1.csv](https://github.com/crtallent/Credit_Risk_Analysis/tree/main/Resources)
* All code can be found [here](https://github.com/crtallent/Credit_Risk_Analysis).

## Calculations

The following matrices were measured to evaluate the performance of each method (TP = true positives, FP = false positives, FN = false negatives, TN = true negatives):

1. Accuracy: the difference between predicted and actual values (TP + TN /(TP + FP + TN + FN)
2. Precision: the number of true positives divided by the number of all positives (TP/(TP + FP))
3. Sensitivity (aka Recall): TP / (TP + FN)
4. F1 = 2 * precision * sensitivity / (precision + sensitivity)

## Results

The preceding information was gathered for each of the matrices below. 

1. Naive Random Oversampling - Balanced Accuracy Score: 68%, Precision: 99%, Recall: 44%, F1 score: 61%
<img src="https://github.com/crtallent/Credit_Risk_Analysis/blob/main/Resources/Images/NRO.png" />
2. SMOTE Oversampling - Balanced Accuracy Score: 63%, Precision: 99%, Recall: 63%, F1 score: 77%
<img src="https://github.com/crtallent/Credit_Risk_Analysis/blob/main/Resources/Images/SMOTE.png" />
3. ClusterCentroids Undersampling - Balanced Accuracy Score: 63%, Precision: 99%, Recall: 44%, F1 score: 61%
<img src="https://github.com/crtallent/Credit_Risk_Analysis/blob/main/Resources/Images/Cluster.png" />
4. SMOTEENN Combination Approach - Balanced Accuracy Score: 52%, Precision: 99%, Recall: 61%, F1 score: 75%
<img src="https://github.com/crtallent/Credit_Risk_Analysis/blob/main/Resources/Images/SMOTEENN.png" />
5. BalancedRandomForest Classifer - Balanced Accuracy Score: 87%, Precision: 99%, Recall: 87%, F1 score: 93%
<img src="https://github.com/crtallent/Credit_Risk_Analysis/blob/main/Resources/Images/BRF.png" />
6. EasyEnsemble Classifer - Balanced Accuracy Score: 94%, Precision: 99%, Recall: 94%, F1 score: 97%
<img src="https://github.com/crtallent/Credit_Risk_Analysis/blob/main/Resources/Images/EEC.png" />

## Summary

In summary, all of the algorithms had high precision (99%), correctly identifying the vast majority of high-risk loan applications. However, the accuracy of each method was much lower for sensitivity (meaning that low-risk applications were flagged as high-risk). We did see these numbers improve when we used the ensemble classifer models. The BalancedRamdomForest Classifer had a balanced accuracy score of 87% and a sensivity score of 87% as well, which is much higher than what we saw in the previous models. However, the EasyEnsemble Classifer surpassed these results with an accuracy score and sensitivity score of 94%, and an F1 score of 97%. This F1 score is also much higher than previous models, indicating that there is not a huge imbalance between precision and sensitivity. While sensitivity is only at 94%, this indicates that only a small portion of low-risk applications will be classified as high-risk. While this model is the most effective at predicting whether an application should be approved, it would be advisable for all applications flagged during the machine learning process for further review to ensure they are not incorrectly identified. In this case, higher precision may be more important than sensitivity because approving high-risk loans that clients cannot pay back could cost a company a lot of money. 

