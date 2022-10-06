# Credit_Risk_Analysis



## Overview of the analysis:

We will use the machine learning tools to predict credit risks.  The credit card dataset from LendingClub is very imbalanced data, i.e. the good credit customers are unproportionally larger than risky credit customers.

We will use RandomOverSampler, SMOTE, ClusterCentroids, and SMOTTEENN algorithms to sample the data and use LogisticRegression to classify the risky credit customers.  Then we will use two ensemble models, BalancedRandomForestClassifier and EasyEnsembleClassifier to make the prediction about the credit risks.



## Results:

Here is the summary table of the results and we also put screen shots after the table:

|    Machine Learning Methods    | Balanced Accuracy Score | Precision Score | Recall Score |
| :----------------------------: | :---------------------: | :-------------: | :----------: |
|       RandomOverSampler        |   0.8329268702127463    |      0.99       |     0.07     |
|             SMOTE              |   0.8388510243681058    |      0.99       |     0.87     |
|        ClusterCentroids        |   0.8125920403078661    |      0.99       |     0.76     |
|           SMOTTEENN            |   0.8486159800498291    |      0.99       |     0.86     |
| BalancedRandomForestClassifier |   0.7189045582528318    |      0.99       |     0.97     |
|     EasyEnsembleClassifier     |   0.9322154970408173    |      0.99       |     0.94     |



1. #### RandomOverSampler Over Sampling

​		Accuracy Score:

![image-20221005205010626](Resources\image-20221005205010626.png)

​		Classification Report:

![image-20221005204938392](Resources\image-20221005204938392.png)



2. #### SMOTE Over Sampling

​		Accuracy Score:

![image-20221005205208717](Resources\image-20221005205208717.png)

​		Classification Report:

![image-20221005205237785](Resources\image-20221005205237785.png)



3. #### ClusterCentroids Under Sampling

​		Accuracy Score:

![image-20221005213001101](Resources\image-20221005213001101.png)

​		Classification Report:

![image-20221005213025572](Resources\image-20221005213025572.png)



4. #### SMOTTEENN Combined Over Sampling and Under Sampling

​		Accuracy Score:

![image-20221005205714187](Resources\image-20221005205714187.png)

​		Classification Report:

![image-20221005205739773](Resources\image-20221005205739773.png)



5. #### BalancedRandomForestClassifier

​		Accuracy Score:

![image-20221005210119649](Resources\image-20221005210119649.png)

​		Classification Report:

![image-20221005210150318](Resources\image-20221005210150318.png)



6. #### EasyEnsembleClassifier

​		Accuracy Score:  

![image-20221005213105038](Resources\image-20221005213105038.png)

​		Classification Report: 

![image-20221005213128080](Resources\image-20221005213128080.png)





### **Summary:** 

For Balanced Accuracy Scores, the EasyEnsembleClassifier method is the highest 0.93.  For Precision Scores, the 6 models are same, all 0.99.  For Recall Scores, the highest is BalancedRandomForestClassifier with score of 0.97.

When considering all six models, we recommend EasyEnsembleClassifier model because it has high Accuracy score of 0.93, high Precision score of 0.99 and high Recall score of 0.94.
