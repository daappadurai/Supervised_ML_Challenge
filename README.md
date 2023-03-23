# Supervised ML Challenge

## **Overview:**
The goal of this project it is to determine a suitable model for detecting “high risk” loan applications. A total of six models are tested three based on sampling and two based on random forest classifiers. The challenge of developing a model for high risk loan application is the disproportionate number of samples available for classification. Out of the 68,817 files available in the dataset evaluated about 347 or 0.5% of the dataset are high risk applications and this poses a significant challenge to train and test the model with this dataset. It is however, the nature of reality as only fewer applications in the general pool of applicants are actually high risk. Five out of the six models address the problem of disproportionate sample size within the categories using the scikit learn library’s imbalance learning module. The five models being tested or as follows.

## **Model	Accounts of disproportionate sampling:** ##

Random Over Sampler (No)
SMOTE Over Sampling	(Yes)
Undersampling	(Yes)
SMOTEEN	(Yes)
Balanced Random Forest Classifier	(Yes)
Easy Ensemble Classifier	(Yes)
	

## **These five models are evaluated based on the following criteria:** ##

1.	Model Accuracy: Percentage variation observed in the target variable (high (0) or low risk (1)) explained by a given model.
2.	 Model Precision: The fraction of the total true positives (high risk or 0) to the total sum of true positives and false positives.
3.	Model Sensitivity: The fraction of the total true positives (high risk or 0) to the toal sum of the true positives and false negatives.
4.	Hormonic Mean f1-score: Depends on the model precision and sensitivity. Higher the f1-score better the model.
5.	Number of false positive cases: The number of cases that were wrongly flagged as high risk applications.

Based on the above criterion, Easy Ensemble method has consistently shown to be a better model compared to all the other models the details of the analysis is presented below.

## **Model Accuracy:** ##

The model accuracy for all the five models is listed in the bar chart below. The Easy Ensemble classifier has the highest accuracy of 0.9316 or 93.16% of the variation observed in the dataset is captured by this model. All the other models are at least 15-40% lower in its accuracy. 



## **Model Precision:** ##

The model precision for detecting high risk applications is consistently lower for all three models dependent on sampling methods. The random forest classifiers that take into account the disproportionate nature of the sample dataset gives a better precision score. Only Easy Ensemble classifier has the highest precision score of close to 0.1. Though a score close to 0.9 or higher is generally higher, compared to all the other models, Easy Ensemble classifier has the best precision score.

## **Model Sensitivity:** ##

Model sensitivity is much higher compared to precision score is much higher, sensitivity takes into the account the number of false negatives, which is lower for all the models. Again, Easy Ensemble classifier has the best model sensitivity score of 0.92

## **Hormonic Mean f1 score:** ## 

F1 score takes into account the precision and sensitivity and gives an overall scoring for the model. Ensemble classifier has the highest f1 score of 0.16. Though a score close to 1 is ideally preferred, compared to all the other models which have scores ranging from 0.02-0.06, Easy Ensemble classifier has the highest f1 score.

## **Number of false positive cases:** ##

This is a graph of cases that were wrongly flagged as high-risk cases. This is where it becomes evident that Ensemble classifier compared to other models is not only good at detecting high risk application, but it also has the lowest number of cases compared to other models that were shows a higher number of wrong classifications.

## **Summary:** ##

Based on the above five criterion, the Easy Ensemble classifier has proved to the best model in predicting high risk application. Though sampling techniques are an attempt to address the disproportionate sample size between categories, they do not significantly improve the precision, sensitivity and the f1 scores. Though Easy Ensemble classifier is better model, it is still not a good model as the f1 score is 0.16, a desirable f1 score is 0.9 or above.

## **Limitations of the analysis:** ##

1.	Though Easy Ensemble classifier is better than all the other models, a conclusion based on statistics cannot be reached because all these models are evaluated only once for a sample(dataset) size, n =1. When these models are tested for a significant number of datasets, then, a conclusion based on statistics can be reached. 
2.	Though none of these models have proved to be useful, the real problem is the dataset rather than the model. The limitation that fewer datapoint are available to determine high-risk application detection is the root cause of the problem. With more datapoints, this problem can easily be circumvented. 
