# # Machine Learning Trading Bot

In this assignment, financial Python programming skills will be used with machine learning to imporve algorithmic trading systems. For this purpose, I will improve an exisiting algorithmic trading systems with machine learning algorithms that can adapt to new data. 

Data source: CSV file

Packages Used This project leverages python 3.7

Installation Guide: The application requires the below programs to be installed

Python
Pandas
Numpy
SKlearn

The steps followed and the results are provided below: 

1. Establish a Baseline Performance using SVC Classifier tool
Results: During the initial periods, the strategy returns are in line with the actual returns. However, as time passed, the strategy returns imporved       over the actual retuns as depcicted by the picture below.
![SVC_Initial_MLreturns_trg_3_smas_4_smal_100](https://user-images.githubusercontent.com/96159292/161206487-ba4fe710-b022-4a3f-aca8-173c8d636bd4.png)
        
2. Tune the Baseline Trading Algorithm uisng by tuning or adjusting, the model’s input features for SVC Classifier. Input festures adjusted include: a. adjusting the size of the training dataset; b.Adjusting the windows for the algorithm
Results: As described in the pandas file, tried several options out and the best option is the one where training is performed based on 6 months data       as it seems to be the sweet spot that avoids overfitting and under fitting. Results of the various options are attached.
a. Results when the SMA short is taken as 2 days and SMA long is taken as 100 days (3 Months Trainign Data)
![SVC_Initial_MLreturns_trg_2_smas_4_smal_100](https://user-images.githubusercontent.com/96159292/161207336-e078eb36-4511-4368-ab16-7c0c7af0b5d9.png)
b. Results when the SMA short is taken as 3 days and SMA long is taken as 50 days (3 Months Trainign Data)
![SVC_Initial_MLreturns_trg_3_smas_3_smal_50](https://user-images.githubusercontent.com/96159292/161207337-d2a35b65-fe7f-49dc-aa9d-63cef5fd11aa.png)
c. Results when the SMA short is taken as 7 days and SMA long is taken as 150 days (3 Months Trainign Data)
![SVC_Initial_MLreturns_trg_3_smas_7_smal_150](https://user-images.githubusercontent.com/96159292/161207839-40b8221f-8194-4655-b118-9f35f5df9123.png)
d. Results when the SMA short is taken as 7 days and SMA long is taken as 200 days (3 Months Trainign Data)
![SVC_Initial_MLreturns_trg_3_smas_7_smal_200](https://user-images.githubusercontent.com/96159292/161207840-630e6911-288e-4961-b7d4-5cb683dcb266.png)
e. Results when the SMA short is taken as 4 days and SMA long is taken as 100 days (6 Months Trainign Data)
![SVC_Initial_MLreturns_trg_6_smas_4_smal_100](https://user-images.githubusercontent.com/96159292/161207844-8cbf6aea-6709-479c-8d66-10b067838814.png)
f. Results when the SMA short is taken as 7 days and SMA long is taken as 200 days (6 Months Trainign Data)
![SVC_Initial_MLreturns_trg_6_smas_7_smal_200](https://user-images.githubusercontent.com/96159292/161207847-ff33f00b-5652-4b74-b1b8-7c6c65b0c21e.png)
g. Results when the SMA short is taken as 4 days and SMA long is taken as 100 days and the Trainig Period is taken as 9 Months 
![SVC_Initial_MLreturns_trg_9](https://user-images.githubusercontent.com/96159292/161207850-5c1818e7-fb12-4c98-a7c4-c02f0d5c6055.png)
h. Results when the SMA short is taken as 4 days and SMA long is taken as 100 days and the Trainig Period is taken as 6 Months 
![SVC_Initial_MLreturns_trg_6](https://user-images.githubusercontent.com/96159292/161207848-3602d2cf-ff66-4eac-856d-c9ea89f4e49a.png)

As can be seen from the above, option h provides the best strategyic return of all the available options including the initial option for this ML Classifier.

    
3. Evaluate with New Machine Learning Classifiers - AdaBoost
Results: AdaBoost Classifier has been selected as an alternative method as it performs particularly well in cases where other methods fail and the margin between the decision is not particularly high. However, as can be seen from the results below, the model did not perform particularly well.
![AdaBoost_MLreturns](https://user-images.githubusercontent.com/96159292/161208592-93808f0c-318b-408d-a79e-4e5ccbbd3754.png)

Evaluation Report
SVC Classifer performed better than the AdaBoost Classifier, in tis case. Within SVC classifer, the best results are obtained when the model is trained for 6 months (with SMA short of 4 days and SMA long of 100 days), as this seems to be the sweet spot that resulkts in optimal fitting. 
The final results with the winning comination is provided below. However, it may be noted that with this option there are period where the strategic returns performed worse than the actual retuns but the final result is that the cumulative retuen surpassed all other options. For an investor, who is risk averse, the original configuration comp0rising of 3 months of traning date (with SMA short of 4 days and SMA long of 100 days) is more palatable.
![SVC_Initial_MLreturns_trg_6](https://user-images.githubusercontent.com/96159292/161207848-3602d2cf-ff66-4eac-856d-c9ea89f4e49a.png)


Contributors: Brought to you by Ram Atmakuri (ram.atmakuri@outlook.com)

License [MIT] (https://choosealicense.com/licenses/mit/)
