# Employee-Attrition-prediction

Introduction: 
    Our task was to predict employee attrition for the sales team of an Insurance Company which is struggling with high attrition rate. We have the monthly information for some employees for year 2016 and 2017 which includes input features for both train and test data. We are supposed to predict whether current employees, whose id is given in a separate csv file, will be leaving the organization in the upcoming two quarters (01 Jan 2018 - 01 July 2018) or not.
 
Approach :

•	In this problem we are not provided with target variable explicitly. 
•	Last working Date is used to find the target variable. 
•	If Last working date is given then that person would have resigned in that month. But he would have decided about resigning in previous quarter itself. We could see some changes in the employee behaviour in past 2 quarters itself. And we also have notice period. Inorder to predict if employee will resign in next 2 quarters. We have considered that employees whose attrition is 1 in given quarters will have attrition as 1 in previous 2 quarters as well
•	We have introduced new features like rating increased or decreased, no of promotions based on joining designation, salary increased or not, last business value to build the model 

Model Building:

We have used different algorithms like decision tree classifier, Random Forest Classifier and AdaBoost Classifier to get predictions 
With Random Forest Classifier we were able to get good F1 score of 0.79 and accuracy of 0.81
We tried many approaches with few new features and attrition status as 1 only for the month they resigned and remaining as 0 and used smote to handle imbalanced dataset. There we were able to get good accuracy of 92% but f1 score is very less. Our scoring criteria is f1 score. So we chose this as our final approach
