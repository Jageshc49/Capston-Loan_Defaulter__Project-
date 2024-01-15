# Capston-Loan_Defaulter__Project-
Welcome to this project for detecting the Defaulters in loan payment and in this Project I will be performing the Exploratory Data Analysis on each and every columns for the Loan Defaulter data, and later on will try to put up the data to test for the same and will try to run some machine learning alogrithms just to predict the missing values for the Loan Defaulter Data set. we used preprocessing, Descriptive Analysis, Predictive Analysis (Regression Model: (Linear Regression) with Decision Tree Regressor with Random Forest Regressor)) Predicted with accuracy more than 80%.
            
# Model Accuracies:
Model	Accuracy
Random Forest with Randomized search CV	82.09
Logistic Regression with Grid search CV	83.18
Support Vector Machine with Grid search CV	82.50
K Nearest Neighbors with Grid search CV	77.40
Bagging with Base estimator as Random Forest	84.10
Bagging with Base estimator as Logistic Regression	83.10
AdaBoost Classifier	83.60

check out our project report to find out why we used these models
Technologies:
Programming Language: Python
Libraries: Pandas, Scikit-learn, Matplotlib, Seaborn

 Loan Defaulter: Exploratory Data Analysis based on Prediction
 ![image](https://github.com/Jageshc49/Capston-Loan_Defaulter__Project-/assets/155012338/14b1a409-6ebe-4d5c-b79c-3b6ceb8e6eb8)

A.	Visual representation of the correlation by Heatmap
Based on the correlation, we can infer that below columns have high correlation –
	Credit_ Amount, Loan_ Annuity, Employed_ Days, Client_ Occupation, Type_ Organization  
Below are the columns have a high skewness bases on the correlation –
	Client_ Income, Client_ Family_ Members, Child_ Count, Client_ Housing_ Type, Default
 In the above image you can see that -1 in the Red highlighted that have a very lower rate correlation.

Rest miner negatives & miner positives in yellows that you can see in above image.
Analyses Categorical variables with respect to Target variable
![image](https://github.com/Jageshc49/Capston-Loan_Defaulter__Project-/assets/155012338/692c955b-fdff-4112-b8ef-7eb44f1593db)

 
From the above plot we can see that,

•	Female customers pay loan amount on time and banks can target more female customers for lending loan.
•	Service customers can be targeted to lend loans as they have higher percentage of making payments on time.
•	Customers with secondary education and Graduation are most likely to make payments when compared to customers with Post Grad.
•	Married customers have paid loan amount on time when compared to widows.¶
•	Customers owning House/family are most likely to make payments on time compared to those living in Rental and Shared.
•	Realty agents have high repayment percentage on time as bank will think to lending a big loan amount to them.
•	Laboure’s have high repayment percentage. Hence banks can think of lending small amount loans to them.
Distribution of Loan _ Annuity
![image](https://github.com/Jageshc49/Capston-Loan_Defaulter__Project-/assets/155012338/a0005a9b-580c-4297-857a-aca0fe22a804)

 
We can infer from the above image that- 
•	We take a look at Loan_ Annuity column as we can see that there are outliers at 22500. But there is no much difference between the mean and median, i.e., mean is 2712.48 and median is 2499.75.
•	After the describe of Loan_ Annuity columns we can impute the outliers with Median here.

Client_ Income and Client_ Income _Type
![image](https://github.com/Jageshc49/Capston-Loan_Defaulter__Project-/assets/155012338/4cfb13ec-967d-4b4b-a513-16b84254c1c7)

 ![image](https://github.com/Jageshc49/Capston-Loan_Defaulter__Project-/assets/155012338/2c4ca3f6-69c7-447f-945d-9fb6e161eaa8)

 
•	Most of applicant are working.
•	Applicants on Maternity Leave, Businessman and Student have lowest percentage of Defaulters.
•	Commercial, Service, Retired and Govt job have a higher percentage of Defaulters.
•	Female applicant is more than the male applicant 
•	Defaulter percentage is higher for female applicant.
Insights from Numerical Bi- Variate Analysis
![image](https://github.com/Jageshc49/Capston-Loan_Defaulter__Project-/assets/155012338/1fd2ba22-54ed-4398-9a8c-b552e472bac1)
![image](https://github.com/Jageshc49/Capston-Loan_Defaulter__Project-/assets/155012338/71b6fef1-7e04-4fb6-881a-d746df382b77)

 
 

Insights,
•	There are more re-payers’ rate when the loan annuity is more than 10k, that means applicants with 10k annuity will more likely to repay their loans, but their frequency is low.
•	Whose applicant’s income is 50k or more than 50k who has 1 car and more than 2 cars.


B. Univariate and Bivariate Analysis by using Histogram
![image](https://github.com/Jageshc49/Capston-Loan_Defaulter__Project-/assets/155012338/c44ec7cf-3730-4114-b715-ff9d8119dd68)
 

 From the above Histogram plot we can say that following below points:
	Whose income is less than Rs.40000. He/ She doesn’t have home and whose income is above Rs.40000. He/ She does have home.
	Whose income is less than Rs.60000, his loan is active and whose income is above Rs.60000, his loan is not active.
	Whose income is above Rs.40000 that amount is credited more than Rs. 2.5 lac. And whose income is less than Rs.20000 that amount is credited less than Rs.1 lac.
	Whose income is more than Rs. 20000 that his/ her is not default and whose income is less than Rs.20000 that She/ He is default in term of paying loan. 
	Whose income is more than Rs.20000 as client city rating is *2.0 and whose income is less than Rs.20000 as client city rating is *1 – 3*.
	Whose income is more than Rs.20000. So, client family member count is 2 and whose income is less than Rs. 20000. So, client family member count is more than 2.
	Whose income is less than Rs. 20000 as he/she is socially defaulting more than 1 times and whose income is more than Rs.20000 as he/she is not defaulting socially.
   
B.	Visual representation of Logistic Regression and KNN by using Confusion Matrix

I.	Visual representation of KNN-
![image](https://github.com/Jageshc49/Capston-Loan_Defaulter__Project-/assets/155012338/005a6962-dfdd-4b99-8550-f4d311f92e13)

 


We can infer below point from above image:
	Top left quadrant= Actual value is [0] and predictive value is [0] that is True positive and the data calculated is 32650.
	Bottom left quadrant = Actual value is [1] and predictive value is [0] that is False negative and the data calculated is 2808.
	Top right quadrant = Actual value is [0] and predictive value is [1] that is False positive and the data calculated is 913.
	Bottom right quadrant = Actual value is [1] and predictive value is [1] that is True negative and the data calculated is 186.

II.	Visual representation of Logistic Regression-
![image](https://github.com/Jageshc49/Capston-Loan_Defaulter__Project-/assets/155012338/66669f78-8f4b-46ef-b3bf-27c52c4e4dd6)

 

We can infer below point from above image:
	Top left quadrant= Actual value is [0] and predictive value is [0] that is True positive and the data calculated is 33563.
	Bottom left quadrant = Actual value is [1] and predictive value is [0] that is False negative and the data calculated is 2994.
	Top right quadrant = Actual value is [0] and predictive value is [1] that is False positive and the data calculated is 0.
	Bottom right quadrant = Actual value is [1] and predictive value is [1] that is True negative and the data calculated is 0



Thanks,
Jagesh Chauhan
