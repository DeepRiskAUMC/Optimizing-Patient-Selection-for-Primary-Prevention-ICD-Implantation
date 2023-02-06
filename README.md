# Optimizing-Patient-Selection-for-Primary-Prevention-ICD-Implantation

#Overview
This repository contains code for pre-processing and analyzing ECG data collected from two sites. 

##ECG Feature Extraction and Machine Learning Model
This project aims to extract features from ECG time-series data and develop machine learning models to predict the risk of ICD non-benefit. The pre-processed ECGs were characterized by 65 unique features calculated using tsfresh algorithm. The feature selection approach combined the Benjamini-Yekutieli procedure and a recursive feature elimination algorithm. The machine learning models used in this project are support vector machines (SVM), extreme gradient boosting algorithms (XGBoost), and random forest (RF) classifiers. The interpretation of individual predictions was explained using the SHAP method and mean waveforms for predicted high risk and predicted low risk of ICD non-benefit in the external patient cohort were displayed.

##Requirements
-Python 3.6 \n
-tsfresh version 0.12.0
-scikit-learn library version 1.1.1.
-XGBoost library version 1.6.2.
-numpy
-pandas
-h5py 3.7.0.
-pydicom

##Usage
The detailed description of ECG pre-processing and feature extraction is provided in the Supplemental Methods. To use this project, first extract the ECG features using tsfresh version 0.12.0 in Python 3.6. Then, perform the feature selection and model training using the scikit-learn and XGBoost libraries. The internal model evaluation was performed by repeated stratified k-fold cross-validation with k=10 and 5 repeats. The performance of the final model was evaluated on the external testing cohort. The interpretation of individual predictions can be explained using the SHAP method.
