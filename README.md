# Credit_Risk_Analysis
Module 17 Challenge

## Overview

Jill would like for us to evaluate several models to see if we can find one that can accurately identify if a loan to a customer would be in risk of default or not.

Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Because of this Jill asked me to employ different techniques to train and evaluate models with unbalanced classes. Jill asked me to use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, I have been requested to oversample the data using the RandomOverSampler and SMOTE algorithms, and undersample the data using the ClusterCentroids algorithm. Then, I'll need to try a combined approached of over- and undersampling using the SMOTEEN algorithm. Next, I'll compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. 

## Purpose

To complete this task, I will use skills learned in this module regarding Supervised Machine learning.  I'll use imbalanced-learn libraries, scikit-learn libraries, Jupyter Notebook and Python to test out several algorithms and models such as :
  * RandomOverSampler
  * SMOTE
  * ClusterCentroids
  * SMOTEEN
  * BalancedRandomForestClassifier
  * EasyEnsembleClassifier

### Deliverable 1

#### Random Over Sampling - Naive RandomOverSampler

  * An accuracy score for the model is **0.8325468421491353**
  
  * A confusion matrix has been generated
  
  ![NaiveRandomOverSampler_confusion_matrix](Images/NaiveRandomOverSampler_confusion_matrix.png)
  
  * An imbalanced classification report has been generated
  
  ![NaiveRandOverSamp_imbal](Images/NaiveRandOverSamp_imbal.png)
  
#### Oversampling - SMOTE

  * An accuracy score for the model is **0.8440938486973113**
  
  * A confusion matrix has been generated
  
  ![SMOTEOverSampler_confusion_matrix](Images/SMOTEOverSampler_confusion_matrix.png)
  
  * An imbalanced classification report has been generated
  
  ![SmoteOverSamp_Imbal](Images/SmoteOverSamp_Imbal.png)

#### Undersampling - ClusterCentroids

  * An accuracy score for the model is **0.8203882595930314**
  
  * A confusion matrix has been generated
  
  ![ClusterCentroidUnderSampler_confusion_matrix](Images/ClusterCentroidUnderSampler_confusion_matrix.png)
  
  * An imbalanced classification report has been generated
  
  ![ClustCentUndSamp_imbal](Images/ClustCentUndSamp_imbal.png)
  
### Deliverable 2

#### Combination of (Over and Under) Sampling - SMOTEEN 

  * An accuracy score for the model is **0.844016280135965**
  
  * A confusion matrix has been generated
  
  ![SMOTEENOverUnderSampler_confusion_matrix](Images/SMOTEENOverUnderSampler_confusion_matrix.png)
  
  * An imbalanced classification report has been generated
  
  ![SmooteenImbal](Images/SmooteenImbal.png)
 
### Deliverable 3

#### Ensemble Learners - Balanced Random Forest Classifier

  * An accuracy score for the model is **0.7837130912576757**
  
  * A confusion matrix has been generated
  
  ![BalancedRandomForestClassifier_confusion_matrix](Images/BalancedRandomForestClassifier_confusion_matrix.png)
  
  * An imbalanced classification report has been generated
  
  ![BRFC_Imbal](Images/BRFC_Imbal.png)
  
  * The features are sorted in descending order by feature importance

#### Easy Ensemble Classifier

  * An accuracy score for the model is **0.931601605553446**
  
  * A confusion matrix has been generated
  
  ![EasyEnsembleClassifier_confusion_matrix](Images/EasyEnsembleClassifier_confusion_matrix.png)
  
  * An imbalanced classification report has been generated
  
  ![EEC_Imbal](Images/EEC_Imbal.png)
  
  ## Summary
  
  The resampling models did not generate an acceptable model. Low F1 score
  
  Although not terrific, The Easy Ensemble Classifier model did the best in classifying the loan status with an f1 score of
