# Supervised_Machine_Learning
## Written analysis for the Module 17 challenge (STOCK. No Extension)

In my project, I created multiple machine learning models using multiple different sampling and re-sampling techniques. The methods that I had to use were: Random Oversampling, SMOTE Oversampling, ClusterCentroid undersampling, and a combination method using SMOTEEN.


#### Random Oversampling Model

The Random Oversampling method takes random datapoints as a means to oversample the minority class so that it is balanced with the majority class.

The Precision Scores for the Random OverSampling Model consisted of the following:
high-risk: 0.01
low-risk: 1.00

The precision scores tell us that the model was very precise at identifying those with low-risk loans. However, it's precision score was much lower when somebody was predicted to have a high risk loan, what this means is that there's a likely hood that somebody who is predicted low risk is most likely low-risk, and somebody high risk may not necessarily be so.

The model returned the following Recall(Sensitivity) scores:
High-risk: 0.74
Low-Risk: 0.61

The Recall scores tell us that the model was actually more sensitive when it comes to detecting high-risk loans verses low-risk loans. This is good because it's more important to detect everyone that might have a high risk loan. So the higher sensitivity is good.

The Balanced Accuracy score for this model was about 0.674. What this means is that the model correctly classified a loan type about 67.4% of the time.

#### SMOTE Oversampling Model
The Precision Scores for the SMOTE OverSampling Model consisted of the following:
high-risk: 0.01
low-risk: 1.00

The precision scores tell us that the same story as the Random Oversampling Model. The model was very precise at identifying those with low-risk loans. However, it's precision score was much lower when somebody was predicted to have a high risk loan, what this means is that there's a likely hood that somebody who is predicted low risk is most likely low-risk, and somebody high risk may not necessarily be so.

The model returned the following Recall(Sensitivity) scores:
High-risk: 0.63
Low-Risk: 0.69

The Recall scores tell us that this model was more sensitive to finding low-risk loans compared to the high risk. This isn't exactly preferred because we do want to be successful at correctly classifying high-risk loans. Another concerning metric is that the sensitivity for high risk loans was less than the Random model.

The Balanced Accuracy score for this model was about 0.662. What this means is that the model correctly classified a loan type about 66.2% of the time. This model was less successful in this metric than the Random Model.

#### ClusterCentroids Undersampling Model

The Precision Scores for the ClusterCentroids Undersampling Model consisted of the following:
high-risk: 0.01
low-risk: 1.00

Once again, the precision scores are the same. We can begin to conclude that this may be part of the nature of the data of predicting credit risk. There are simply so few high credit risk situations.

The model returned the following Recall(Sensitivity) scores:
High-risk: 0.73
Low-Risk: 0.59

The Recall scores tell us that this model was much more sensitive to finding high-risk credit risks compared to that of low-risk credit risks. It is a little concerning that the sensitivity is under 60% for Low-Risk, but we should appreciate the 73% for High-Risk.

The Balanced Accuracy score for this model was about 0.661. What this means is that the model correctly classified a loan type about 66.1% of the time. This model was less successful in this metric than the Random Oversampling and the SMOTE Model. This could possibly be attributed to the lower recall on low-risk applications.

#### Combination SMOTEENN Model

The Precision Scores for the Combination SMOTEENN Model consisted of the following:
high-risk: 0.01
low-risk: 1.00

We can rightfully claim this is due to the nature of the data

The model returned the following Recall(Sensitivity) scores:
High-risk: 0.71
Low-Risk: 0.57

Similar to other models, this model was also more sensitive for High-risk than Low-risk. However again, the 57% recall for Low-risk is rather low. The 71% for High Risk did not beat other models.

The Balanced Accuracy score for this model was about 0.662. What this means is that the model correctly classified a loan type with about the same accuracy as the ClusterCentroid Model.

### Recommended model?

In terms of choosing a model to recommend for use. I would say that if I had to pick a model, it would be the Random Oversampling model simply because its performance was better than that of the other models... at least according to what my data is showing me.

The Random Oversampling model had the highest balanced accuracy score of 67.4%, meaning it correctly classified the loans at the highest rate. While this is important, what is more important is that its sensitivity for High-Risk credit was the highest out of all the models. We would rather have a higher sensitivity for High-Risk than not. The reason behind this is that we would rather have some false positives than false negatives. A false positive simply means we were more cautious than necessary, while false negatives would mean that somebody who might ACTUALLY be a large risk could slip through the cracks.

With that being said, I would urge the company to continue to try to find different models to predict credit risk. While the Random Oversampling model was the best, I still think that there is room for improvement in terms of the balanced accuracy score. Being correct 67.4% of the time still means that quite a number of mistakes would be made. Considering how much data could be entering through the company, the number of possible errors could be considerably large.