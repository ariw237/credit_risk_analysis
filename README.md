# credit_risk_analysis
## Overview  
Given a credit card dataset from LendingClub, a p2p lending company, the task at hand is to build and evaluate several machine learning models ability to determine credit risk of individual customers.  This represents an unbalanced classification  problem due to the higher ratio low risk loans over high risk ones. Essentially, a number of metrics or features are used to determine whether/probability a customer belongs in one of two classes: high credit risk, or low credit risk. Since the classes are unbalanced, a couple of oversampling and undersampling and ensemble-based classifiers were evaluated. Of importance here is both recall and precision in terms of being able to catch high risk credit lending profiles, while minimizing false positives.     

### Results  

Logistic Regression was performed using the following models/classifiers designed to compensate for the imbalance:  

* Random Oversampling  
* SMOTE (Synthetic Minority Oversampling)  
* Undersampling  
* Combined Over/Under Sampling  
* Balanced Random Forest  
* Easy Ensemble  

The following Precision and Recall scores were obtained for each method based on credit risk:  

Random Oversampling:  
High Risk/Low Risk Recall:  0.72/0.60    
Balanced Accuracy:  0.66  
![random_oversample](https://user-images.githubusercontent.com/60231630/151751991-e09d6522-bd0a-406e-a1fe-59bce421d668.png)  

SMOTE:  
High Risk/Low Risk Recall:  0.61/0.70    
Balanced Accuracy:  0.66  
![smote_oversample](https://user-images.githubusercontent.com/60231630/151752013-68f53db1-172a-4224-bffa-3e4b1babb243.png)  

Undersampling:  
High Risk/Low Risk Recall:  0.69/0.40   
Balanced Accuracy:  0.54  
![under_sample_cluster_centroid](https://user-images.githubusercontent.com/60231630/151752061-e3beb7e2-eca4-446d-b3c4-415c7d826aec.png)  

Combined Over/Under:  
High Risk/Low Risk Recall:  0.69/0.59  
Balanced Accuracy:  0.63  
![combination_over_undersample](https://user-images.githubusercontent.com/60231630/151752156-d8a5e370-d9e9-4eb9-b1b8-d433cf7ad950.png)  

Balanced Random Forest:   
High Risk/Low Risk Recall:  0.70/0.87  
Balanced Accuracy:  0.79  
![balanced_forest](https://user-images.githubusercontent.com/60231630/151752239-7ceacc3c-5509-4b4e-a580-ba3e07f5f61d.png)  


Easy Ensemble:   
High Risk/Low Risk Recall:  0.92/0.94  
Balanced Accuracy:  0.93  
![easy_ensemble](https://user-images.githubusercontent.com/60231630/151752348-fc60e50d-643b-4663-8b4b-b24c14c046ab.png)  


### Summary  
A goal here is to be able to identify high risk credit profiles with minimal false negatives and low risk profiles with minimal false positives.  All the models exhibited generally poor precision in identifying high risk profiles, however this may be considered acceptable risk due to the cost burden of loan defaults. Along these lines, the Easy Ensemble Classifier model would likely be most appropriate here with high recall for high risk profiles. This model also has a high f1 score in the identification of low risk profiles, indicating a lower rate of false positives which could otherwise be costly.  Nevertheless, if minimizing false positives for high risk profiles is also of high priority, then a different model other than those analyzed here might be warranted.  


  

