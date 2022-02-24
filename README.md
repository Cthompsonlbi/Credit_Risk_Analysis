# Credit_Risk_Analysis
Module 17 Challenge

## Overview

Jill would like for us to evaluate several models to see if we can find one that can accurately identify if a loan to a customer would be in risk of late payment, default or even fraudulent.

Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Because of this Jill asked me to employ different techniques to train and evaluate models with unbalanced classes. Jill asked me to use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

Using the credit card credit dataset from LendingClub, a peer-to-peer lending services company, I have been requested to oversample the data using the RandomOverSampler and SMOTE algorithms, and under sample the data using the ClusterCentroids algorithm. Then, I'll need to try a combined approached of over- and under sampling using the SMOTEEN algorithm. Next, I'll compare two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. 

## Purpose

To complete this task, I will use skills learned in this module regarding Supervised Machine learning.  I'll use imbalanced-learn libraries, scikit-learn libraries, Jupyter Notebook and Python to test out several algorithms and models such as:
  * RandomOverSampler
  * SMOTE
  * ClusterCentroids
  * SMOTEEN
  * BalancedRandomForestClassifier
  * EasyEnsembleClassifier

### Deliverable 1

#### Random Over Sampling - Naive RandomOverSampler

  * An accuracy score of the RandomOversampler model is **0.8325468421491353**
  
  * Below is the confusion matrix that has been generated from this model
  
  ![NaiveRandomOverSampler_confusion_matrix](Images/NaiveRandomOverSampler_confusion_matrix.png)
  
  * Below is the imbalanced classification report that has been generated from this model
  
  ![NaiveRandOverSamp_imbal](Images/NaiveRandOverSamp_imbal.png)
  
#### Over sampling - SMOTE

  * An accuracy score for the model is **0.8440938486973113**
  
  * Below is the confusion matrix that has been generated from this model
  
  ![SMOTEOverSampler_confusion_matrix](Images/SMOTEOverSampler_confusion_matrix.png)
  
  * Below is the imbalanced classification report that has been generated from this model
  
  ![SmoteOverSamp_Imbal](Images/SmoteOverSamp_Imbal.png)

#### Under sampling - ClusterCentroids

  * An accuracy score for the model is **0.8203882595930314**
  
  * Below is the confusion matrix that has been generated from this model
  
  ![ClusterCentroidUnderSampler_confusion_matrix](Images/ClusterCentroidUnderSampler_confusion_matrix.png)
  
  * Below is the imbalanced classification report that has been generated from this model
  
  ![ClustCentUndSamp_imbal](Images/ClustCentUndSamp_imbal.png)
  
### Deliverable 2

#### Combination of (Over and Under) Sampling - SMOTEEN 

  * An accuracy score for the model is **0.844016280135965**
  
  * Below is the confusion matrix that has been generated from this model
  
  ![SMOTEENOverUnderSampler_confusion_matrix](Images/SMOTEENOverUnderSampler_confusion_matrix.png)
  
  * Below is the imbalanced classification report that has been generated from this model
  
  ![SmooteenImbal](Images/SmooteenImbal.png)
 
### Deliverable 3

#### Ensemble Learners - Balanced Random Forest Classifier

  * An accuracy score for the model is **0.7837130912576757**
  
  * Below is the confusion matrix that has been generated from this model
  
  ![BalancedRandomForestClassifier_confusion_matrix](Images/BalancedRandomForestClassifier_confusion_matrix.png)
  
  * Below is the imbalanced classification report that has been generated from this model
  
  ![BRFC_Imbal](Images/BRFC_Imbal.png)
  
  * The screen shot below shows the features sorted in descending order by feature importance.  This is just a small sample of the entire list. Feature importance can provide insight on which features are considered more important than others. Allowing us to modify the dataset further if the models prove to be inconclusive or provide no improvement in detecting high-risk loans.
  
  ![importantfeatures](Images/importantfeatures.png)

#### Easy Ensemble Classifier

  * An accuracy score for the model is **0.931601605553446**
  
  * Below is the confusion matrix that has been generated from this model
  
  ![EasyEnsembleClassifier_confusion_matrix](Images/EasyEnsembleClassifier_confusion_matrix.png)
  
  * Below is the imbalanced classification report that has been generated from this model
  
  ![EEC_Imbal](Images/EEC_Imbal.png)
  
  ## Analysis Summary
  
Because each model appeared the be sufficient at identifying low-risk loans, I created the table below consolidating the imbalanced summary reports of each model's high-risk loan results. 
  
| Model          | Precision      | Recall         | F1
| ---------------| ---------------| ---------------| ---------------
| RandomOverSamp | .03  | .82 |.06
| Smote | .04 | .82 |.07
|ClusterCentroids |.02|.88 |.04
|SMOTEEN |.03|.83 |.06
|BalancedRandomForest |.03|.69 |.06
|SMOTEEN |.09|.94 |.16



As I mentioned above, all the resampling models did a sufficient job of identifying loans that are considered low-risk status.  However, the models struggled with identifying potentials loans that are considered high-risk. Meaning, the models struggled identifying loans that were high-risk of being paid late, or that were fraudulent or that could fall into default.  None of the resampling models provided improvment as each had a low f1 score and low precision results that ranged from .04 to .06.  The ensemble models, particularly SMOTEEN proved to be slightly better in identifying high-risk loans.  Their precision score, recall score, and f1 score were better than the resampling models.  The SMOTEEN f1 score of 16 is by far better than all the resampling f1 scores but, .16 is still not ideal.

If one must move forward with one of these models, then the SMOTEEN would be the recommendation.  However, if more time is available, perhaps going back to the dataset and reshaping the data by identifying columns that are not deemed as important to the decision-making process or model creation process and have them removed.  The feature importance screenshot captured in Deliverable 3 could identify data that is not important to the model and allow us to remove it and lessen its impact on the model. This would allow greater weight to fall upon the key components necessary to identify high-risk loans and potentially improve the accuracy of the models.
