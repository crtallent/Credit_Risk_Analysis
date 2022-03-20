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
4. f1 = 2 * precision * sensitivity / (precision + sensitivity)

## Results

The preceding information was gathered for each of the matrices below. 

1. Niave Random Oversampling
<img src="https://github.com/crtallent/Credit_Risk_Analysis/blob/main/Resources/Images/NRO.png" />
2. SMOTE Oversampling
<img src="https://github.com/crtallent/Credit_Risk_Analysis/blob/main/Resources/Images/SMOTE.png" />
3. ClusterCentroids Undersampling
<img src="https://github.com/crtallent/Credit_Risk_Analysis/blob/main/Resources/Images/Cluster.png" />



