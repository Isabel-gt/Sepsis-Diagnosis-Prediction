# Sepsis-Diagnosis-Prediction

## Overview of the Project
Application of data anlaysis and machine learning to design an end-to end machine learning pipeline for predicting binary outcomes from a real-world dataset of 27,187 patients.

<p align="justify">The analysis, the visualizations and the models were created using Python.</p>


## Feature Engineering 

### Data Cleaning

<p align="justify">The data was analyzed and examined using Python. During this stage different visualizations were created to showcase each feature such as creatine, oxigen saturation, bilirubin, etc. Also outliers were identified and the data was cleaned. Below there is an example of one of the Box Plots that were created.</p>

<img width="400" alt="0" src="https://github.com/Isabel-gt/Sepsis-Diagnosis-Prediction/blob/3fe0ce17d722547869e1a301f0e7af6e23521796/Images/1.png">

<p align="justify">Summary statistics and plots were designed. The **Vital Signs**, **Laboratory Values**, and the **Demographics** were grouped and plotted by Sepsis *(0 indicating NO sepsis and 1 indicating patients with sepsis)*. Moreoever, the distribution of **Vital Signs**, **Laboratory Values**, and the **Demographics** was plotted as well.An example of the **Vital Signs** by sepsis is shown below.</p>

<img width="400" alt="0" src="https://github.com/Isabel-gt/Sepsis-Diagnosis-Prediction/blob/f16ffe00593cde5a1f6ee9713435d0168c72bf33/Images/2.png">

### Data Processing 

<p align="justify">The measurements were aggregated. Since the dataset was a time-series of patient measurements over 24 to 48 hours, it was tranformed into an appropiate format to later be used for the machine learning model developement. The difference between the value of the measurement of the first hour and the value of the measurement of the last hour for each patient was obtained.<p/>

<p align="justify">By doing that instead of having a dataset with 24 to 48 rows of measurements, now each patient resulted to have a single row.<p/>


## Model Training

### XGBoost Implementation

<p align="justify">An XGBoost model was developed without using any data resampling techniques. The dataset was separated using a *X_train, X_test, y_train, y_test* split<p/>

### XGBoost with Hyperparameter Tuning

<p align="justify">Another XGBoost model was developed but this time **hyperparameted tuning** with **GridSearch Cross Validation** was used.
The Grid was used to search the best set of hyperparametes and their corresponding score.<p/>

<p align="justify">This model was used to predict sepsis in the *X_test* set.<p/>


### Model Performance

<p align="justify">After that, the performance metric were evaluated using a confusion matrix.<p/>

<img width="400" alt="0" src="[https://github.com/Isabel-gt/Sepsis-Diagnosis-Prediction/blob/f16ffe00593cde5a1f6ee9713435d0168c72bf33/Images/2.png](https://github.com/Isabel-gt/Sepsis-Diagnosis-Prediction/blob/cfe5b2d37685353ebd95cc0b9c7aeb82db6d4cb1/Images/3.png)">

<p align="justify">The confusion matrix shows that the model is 95% accurate which indicates that the model performs well.

<p align="justify">The ROC (Receiver Operating Characteristic) curve was plotted to show the trade-off between True Positive Rate and False Positive Rate. In this case the AUC (Area Under the Curve) shows that there is a 92% chance that the model will rank a random positive case higher than a random negative case. This indicated that the model is effective when distinguishing between classes (sepsis or NO sepsis).<p/>

<img width="400" alt="0" src="https://github.com/Isabel-gt/Sepsis-Diagnosis-Prediction/blob/f44b7696053bfd543fd6054ebebcfbbb63c96fb2/Images/4.png">


### Feature Importance

<p align="justify">The feature importance was obtained and it is shown in the graph below. The first feature corresponds to the most important one and so on.<p/>

<img width="400" alt="0" src="https://github.com/Isabel-gt/Sepsis-Diagnosis-Prediction/blob/ffa6299eefdf70f7a4c671ffe1af8e02625c94a3/Images/5.png">


## Results

<p align="justify">The machine learning pipeline was followe and a machine learning model was successfully built to predict sepsis.<p/>








