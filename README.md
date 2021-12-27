# CREDIT CARD FRAUD DETECTION USING SVM
## INTRODUCTION
The dataset is obtained from https://www.kaggle.com/mlg-ulb/creditcardfraud

The dataset comprises of Time, Amount, Class and 28 features(V1 to V28) obtained from PCA. Support vector machines (SVM) will be used for classification. We will make use of the features and Class in classification by using different kernel functions. Linear Kernel, RBF Kernel, Sigmoid Kernel and Polynomial Kernel are the four different types of kernel functions which were tried out.

The dataset contains only 0.172% of fraud cases so it is very unbalanced. The dataset is split as 70% training data and 30% testing data. As the dataset is unbalanced we train the model on 50-50 data of fraud and non fraud cases instead of a highly biased dataset towards non fraud cases. This helps the model to learn better about the fraud cases. We test the models using the same method of 50% fraud cases and 50% non fraudd cases from the test data. This new test data is better to use as compared to the old test data where the non fraud cases were extremely high.


## STEPS
1. Reading and visualising the data
2. Preparing the data for modeling
3. Build and train the model on new_Xtrain and new_ytrain and evaluate the model on accuracy and f1 score for different kernels using new_Xtest and new_ytest.


## CONCLUSION
When we take the case of 50-50 fraud and non fraud cases for both training(new_Xtrain,new_ytrain) and test(new_Xtest,new_ytest) dataset we can see that the f1 score is 94.91 and accuracy is 94.92% for the linear kernel case making it the best performing kernel. The second best performing kernel is the RBF kernel with accuracy 92.97%. In case we use the train(X_train,y_train) and test(X_test,y_test) data set on the model, the model overfits as the datapoints of non fraud cases dominates and the accuracy comes around 99%. Thus, dividing the dataset as 50-50 fraud and non fraud cases for both training and test cases allows the model to learn more about the fraudulent cases.
