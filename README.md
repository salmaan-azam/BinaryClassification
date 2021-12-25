# Binary Classification Probelm 
Objective : Build a Machine Learning Model for classify classes between 0 ana 1.

# Table of Content
*   [Overview](#Overview)
*   [Metrics](#Metrics)
*   [EDA](#EDA)
*   [Feature Selection](#Feature-Selection)
*   [Modelling](#Modelling)
*   [Hardware Configuration Used](#Hardware-Configuration-Used)
*   [References](#References)

## Overview

Dataset has 3910 records and 57 features on which 299 (7.65%) records are dupliactes.
Features are of Numberical Type. It don't have any missing values. The dataset mostly contain zeros.

**Dependent Features Distributions**
![Data Overview](https://github.com/salmaan-azam/BinaryClassification/blob/main/image/1.png)

## Metrics

This Dataset is slightly Imbalance that is why we have choosed AUC Score as a Matrix along with Accuracy. We also Perform Confusion Matrix to know where model is not performing well.

![Data Overview](https://github.com/salmaan-azam/BinaryClassification/blob/main/image/10.png)
![Data Overview](https://github.com/salmaan-azam/BinaryClassification/blob/main/image/11.png)


## EDA

We have used Violin Plot because it gives data distribution diagram for indivitual feature.
We also performed TSNE for getting insight of high-dimensional data into two dimesional plot.
It captures structure in such way that neighboring points of a data in high dimensional space 
will also be the neighbors in the low dimensional space. In a short it preseve neighbourhood structure.
![Data Overview](https://github.com/salmaan-azam/BinaryClassification/blob/main/image/2.png)
![Data Overview](https://github.com/salmaan-azam/BinaryClassification/blob/main/image/3.png)

# Feature Selection

We have tried three methods for Feature Selection:

        1. Using Correlation Matrix : We removed those features whose correlation was more tha 0.5 to some other features 
        2. Mutual Information : We remove those features which contain less information given one features
        3. Using Random Forest Features Importance : We remove those features which have less feature Importance.
        
**Features Importance Plot**
                      
![Data Overview](https://github.com/salmaan-azam/BinaryClassification/blob/main/image/7.png)    


# Modelling

We have three dataset from feature selection steps and we used one full feature dataset for training so
total four set of data are available for training. We used following machine learning models for tarining:

                    1. K Nearest Neighbourhood
                    2. Logistic Regression
                    3. Support Vector Classifier
                    4. XGBoost
                    5. Artificial Neural Network
                                          
**Machine Learning Model Performace Results**

![Data Overview](https://github.com/salmaan-azam/BinaryClassification/blob/main/image/12.png) 

We choose XGBoost Model with Full Feature dataset for train the full dataset and predict result on test dataset.


## Hardware Configuration Used:
* Jupyter Notebook with 8GB RAM

## References:

**Data Source:** arya.ai

1. https://www.youtube.com/watch?v=uMlU2JaiOd8&list=PLZoTAELRMXVPgjwJ8VyRoqmfNs2CJwhVH&ab_channel=KrishNaik
2. https://www.analyticsvidhya.com/blog/2020/10/feature-selection-techniques-in-machine-learning/
3. https://www.analyticsvidhya.com/blog/2020/11/popular-classification-models-for-machine-learning/


