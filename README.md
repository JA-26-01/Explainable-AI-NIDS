# Explainable-AI-NIDS

An approach to detect network instrusion using machine learning paradigms

NIDS has been one of the prime concerns and also of the most researched fields using applied machine learning. The classical machine learning approaches have proved to be efficient in Network Intrusion Detection. I have made an attempt in making a customized ML model for Network Intrusion Detection, using the traditional models, and compared its performance to the exisiting ones.

Explainable AI has been used in order to predict and explain the model's behaviour. I have mainly used the feature importance plot to visualize the dependency of the model on the different attributes present in the data that has been used for training.

#Models used:

1. Decision Tree
2. Random Forest
3. XGBoost
4. A 2-Stacked Ensemble - with the 0th layer consisting of 3 Random Forest Models, and the 1st layer consisting of Logistic Regression as the meta-classifier

#Explainable AI framwork used: ShapLey

#Dataset used:

Train set: https://drive.google.com/file/d/1IjJw8NfuhrYPpVYntN5YE19poWEF4nUP/view?usp=sharing
 
Test set: https://drive.google.com/file/d/1i1l3UuZi6R6QcE2BsW-7JBx6Q1SDSohc/view?usp=sharing

#Mandatory Data Pre-processing

Apart from handling null values and type conversion, Oversampling has been performed in order to balance the dataset, as it is highly skewed.

#Results obtained:

The stacked ensemble performed well than both the Random Forest and Decision Tree classifiers, and was second to XGBoost in performance with respect to precision, accuracy and recall. 

Using ShapLey, the feature importance plot generated indicates that Feature 46 or the PSH Flag Count is the most important feature, according to the ensemble model, in classifying the attacks into the respective classes.

Reference paper: The methodology/ workflow followed is based on the work proposed in the paper below:

T. Zebin, S. Rezvy and Y. Luo, "An Explainable AI-Based Intrusion Detection System for DNS Over HTTPS (DoH) Attacks," in IEEE Transactions on Information Forensics and Security, vol. 17, pp. 2339-2349, 2022, doi: 10.1109/TIFS.2022.3183390.

https://ieeexplore.ieee.org/document/9796558

