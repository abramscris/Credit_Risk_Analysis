# Credit_Risk_Analysis

## Overview

On the following analysis it will be demonstrated the Machine learning statistical algorithms in order to present predictions based on data patterns provided. The method used will be Supervised Learning utilizing a free dataset from LendingClub, a P2P lending service company to evaluate and predict credit risk. 

The techniques used to train and evaluate the dataset are based on unbalanced classification problem due to the number of good loans outweighing the amount of risky loans. Furthermore, the Machine learning algorithms are use to resample the data and more detailed on the Results of this search.

## Results 

To introduce the Machine learning the data was resampled using Python libraries scikit-learn and imbalanced-learn evaluated the results and provide a comparison as on the following image:

 <img src="https://github.com/abramscris/Credit_Risk_Analysis/blob/master/Resources/img1.png" width="400">

With 115,675 loan applications of 2019 data set we refine using the “loan status” in order to show the considered low and high risk what gave the refined amount of 68,817 total applications with current status.

* The method of 75/25% was used to split the data and training vs. testing.

 
 <img src="https://github.com/abramscris/Credit_Risk_Analysis/blob/master/Resources/img2.png" width="400">


## Oversampling – Deliverable 1
At this point of the analysis, we utilize the RandomOverSampler Model, which consists in select randomly from the minority class and adds it to the training set until both classifications are equal. The results classified 51,366 records each as High Risk and Low Risk 
Below we can see the findings:


 <img src="https://github.com/abramscris/Credit_Risk_Analysis/blob/master/Resources/img3.png" width="500">
 
We discovered the accuracy of 65%.


 <img src="https://github.com/abramscris/Credit_Risk_Analysis/blob/master/Resources/img4.png" width="400">

* The High-risk precision rate it was just 1% with the recall at 72% giving this model an F1 score of 2%.
* An on the Low risk we found the precision rate of 100% and recall at 59%.

 <img src="https://github.com/abramscris/Credit_Risk_Analysis/blob/master/Resources/img5.png" width="400">

To further investigation we used the SMOTE (Synthetic Minority Oversampling Technique) Model, similar to RandomOverSamplerincreases this model show the size of the minority class by creating new values based on the value of the closest neighbors to the minority class instead of random selection.

Findings:

* The balanced accuracy score improved to 66%.

 
 <img src="https://github.com/abramscris/Credit_Risk_Analysis/blob/master/Resources/img6.png" width="400">

* Still similar to RandomOverSampler, the High-Risk precision rate continue to 1% with a significant drop of to 63% recall amount and a F1 score of 2%.
* Low Risk had a precision rate of 100% and an also significant improved recall at 69%.


 <img src="https://github.com/abramscris/Credit_Risk_Analysis/blob/master/Resources/img7.png" width="400">
 
 
## Undersampling


Moreover, we have the ClusterCentroids Model, what consists in an algorithm that identifies clusters of the majority class to generate synthetic data points that are representative of the clusters. 
The model identified 246 records each as High Risk and Low Risk.

 <img src="https://github.com/abramscris/Credit_Risk_Analysis/blob/master/Resources/img8.png" width="400">


* Balanced accuracy score was lower than the oversampling models at 54%.


 <img src="https://github.com/abramscris/Credit_Risk_Analysis/blob/master/Resources/img9.png" width="400">
 
* The High-Risk precision rate continue to 1% with a recall of 69% and a F1 score of 1%.
*  Low Risk had a precision rate of 100% and a lower recall at 40%.


 <img src="https://github.com/abramscris/Credit_Risk_Analysis/blob/master/Resources/img10.png" width="400">
 

## Deliverable 2

### Combination sampling 

At this moment of the analysis we utilize the SMOTEENN (Synthetic Minority Oversampling Technique + Edited NearestNeighbors) Model, which consists in combines aspects of both oversampling and undersampling.

* What we found a total of 68,460 records as High Risk and 62,011 as Low Risk.

 <img src="https://github.com/abramscris/Credit_Risk_Analysis/blob/master/Resources/img11.png" width="400">


Findings:

* The balanced accuracy score improved to 64% when using a combined sampling model.


 <img src="https://github.com/abramscris/Credit_Risk_Analysis/blob/master/Resources/img12.png" width="400">
 
*  Then we have High Risk precision rate stay the same at only 1%, however the recall increased to 72% giving this model an F1 score of 2%.
*  The Low Risk still showed a precision rate of 100% with the recall at 57%.
 
 
 <img src="https://github.com/abramscris/Credit_Risk_Analysis/blob/master/Resources/img13.png" width="400">

# Deliverable 3 
## Ensemble Classifiers to Predict Credit Risk
Now we compare two new Machine Learning models that reduce bias to predict credit risk.
Where we had found a total of 51,366 as High Risk and 246 as Low Risk.

 
 <img src="https://github.com/abramscris/Credit_Risk_Analysis/blob/master/Resources/img14.png" width="400">

Using the BalancedRandomForestClassifier Model, two trees of the same size and equal size to the minority class are constructed to represent one for the majority class and one for the minority class.



Findings:
*  The balanced accuracy score increased to 78% for this model.


 <img src="https://github.com/abramscris/Credit_Risk_Analysis/blob/master/Resources/img15.png" width="400">
 
* Where the High Risk precision rate increased to 3% with the recall at 70% giving this model an F1 score of 6%.
* And Low Risk still had a precision rate of 100% with the recall at 87%.


 <img src="https://github.com/abramscris/Credit_Risk_Analysis/blob/master/Resources/img16.png" width="400">
 
* The top feature by importance was "total_rec_prncp" at 7.9% of the total.


 <img src="https://github.com/abramscris/Credit_Risk_Analysis/blob/master/Resources/img17.png" width="400">
 
As last we have the EasyEnsembleClassifier Model, a set of classifiers where individual decisions are combined to classify new examples.

Findings:

* We found a significant increase of balance accuracy of 93%.


 <img src="https://github.com/abramscris/Credit_Risk_Analysis/blob/master/Resources/img18.png" width="400">
 

* The High-Risk precision rate increased to 9% with the recall at 92% giving this model an F1 score of 16%.
*  And the Low Risk still had a precision rate of 100% with the recall now at 94%.


 <img src="https://github.com/abramscris/Credit_Risk_Analysis/blob/master/Resources/img19.png" width="400">
 

## Summary 

After a deep analysis of the data in the different 6 models presented it was clear that the model EasyEnsembleClassifer performed better, giving an accuracy of 93% and 9% of precision on the High Risk prediction. When looking at the sensitivity rates ( recall ) it also performed the best with 92% amount presented.
When performed on Low risk this model also presented the best sensitivity (recall ) on a rate of 94% and F1 score of 97%.

model yielded the best results with an accuracy rate of 93.2% and a 9% precision rate when predicting "High Risk candidates. The sensitivity rate (aka recall) was also the highest at 92% compared to the other models. The result for predicting "Low Risk" was also the highest with the sensitivity rate at 94% and an F1 score of 97%. Therefore, if a model needed to be recommended to perform this type of analysis, then this one would be the clear choice.

## Resources

* Software: Python 3.7.9, Anaconda 4.9.2 and Jupyter Notebooks 6.1.4
