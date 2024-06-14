# Credit Risk Crystal Ball: Predicting Risk with Machine Learning
<img src="https://github.com/NJAimesD/AIAcademyCS/assets/159951082/9249a348-f7f3-46e8-bca0-742d921947ce" width="650" /> 

### Overview and Business Understanding

Credit risk prediction is a crucial process for financial institutions, aiming to assess the likehood of a borrower defaulting on a loan. That way the people not likely to default can more easily access loans with better conditions, while the institutions reduce the risk of financial loss.
There are many techniques to predict credit risk, but Machine Learning (ML) can be used to automate the prediction process, since it learns the patterns associated with a defaulter profile and its use reduces time and resource consumption.
Detecting people with a high risk profile can be a complex task, but still results in a better profit margin for the institution. Also, ML improves the efficiency of the process, and the institution resources can be now used in other areas that require human supervision.

Our team at Deloitte seeks to use different machine learning models to predict the credit risk for different profiles, test them and implement a metric to compare them. Once evaluated, we´ll select the model with the best results, and identify the factors with the highest influence on credit risk for a higher value-add to the client.

#### The Problem:
* Banks receive many loan applications daily.
* Manual approval takes a long time.
* Manual approval can result in more errors and bias.
* Could lose clients to competitors with a superior application process.

#### Benefits of Our Solution:
* A streamlined process for approving loans.
* Higher accuracy in the approval process.
* Higher client satisfaction.
* Loan approval fairness, reducing biases



### Description of Data

**Data Source**: Credit Risk Dataset: (https://www.kaggle.com/datasets/laotse/credit-risk-dataset)

**Exploratory analysis**   
We first reviewed all the variables to understand their meaning.

<img src="https://github.com/NJAimesD/AIAcademyCS/assets/159951082/4d96d12d-fde1-47ea-8751-e23fe36e0add" width="600" />


The target variable in this dataset is loan status There are 11 independent variables used for modeling, with a range of 32,581 to 28,638 non-null values. The average age of the sample population is 27 years old, with an average loan amount of around $10,000 and an average credit history of 5.8 years these descriptive stastics were pulled after removing outliers and nulls.

The target variable in this case, with 78.3% of values indicating non-default and 21.7% indicating default, is significantly unbalanced, a data balancing technique was needed, specifically, SMOTE, that is an oversampling technique used to balance the class distribution of a dataset by creating synthetic minority class samples.The purpose of using SMOTE is to remove biases in our model.

<img src="https://github.com/NJAimesD/AIAcademyCapstone/assets/159951082/0d3f2174-0525-43d2-af43-126b4d85363d" width="600" /> 

#### Correlation matrix
A comparative visual analysis was performed, where we built a correlation matrix for all the variables.  

<img src="https://github.com/NJAimesD/AIAcademyCapstone/assets/159951082/5355d94d-3a12-4858-8514-f387efed3549" width="600" /> 

Checking the variables correlations to the Loan Status, we found that the most correlated variables are  Loan Percent Income, Loan Interest Rate as well as the Loan Grade D, so we would expect this variables to have the greatest impact on the final result, as well as the negatively correlated variables 


<img src="https://github.com/NJAimesD/AIAcademyCS/assets/159951082/e342dfb8-4485-408e-a9e2-703e73397373" width="600" /> 

### Data Understanding and Analysis


<img src="https://github.com/NJAimesD/AIAcademyCS/assets/159951082/625f246c-9091-4396-9d54-768112b26239" width="600" /> 


<img src="https://github.com/NJAimesD/AIAcademyCS/assets/159951082/a180d5ca-ef0f-469d-914c-41f849d4ec6b" width="600" /> 

<img src="ttps://github.com/NJAimesD/AIAcademyCS/assets/159951082/b14064e7-8d38-4b7b-bcda-69aecbf566a4" width="600" /> 

<img src="https://github.com/NJAimesD/AIAcademyCS/assets/159951082/14a7c6dd-6cea-406b-8e36-8770db6a8201" width="600" /> 


### Data processing

### Models evaluated

* Linear Regression: Finds the linear equation that fits the best the data...
* Logistic Regression: The goal is to predict the probability that an instance belongs to a given class or not.
* Ridge Model: Linear regression model that adds a penalty term to the least squares objective, to prevent overfitting by shrinking the coefficients towards zero.
* Random Forest Model: Ensemble learning method that builds multiple decision trees during training and outputs the mode of the classes (classification) or average (regression) of the individual trees.
* Xgboost Model: Gradient boosting algorithm that sequentially builds new models to correct errors of the previous models, using a regularization term to prevent overfitting and achieve higher prediction accuracy.



#### Comparison

For evaluating the model performance we´ll use Precision, Recall and F1-Score.
Precision: refers to the percentage of profiles the model identifies as defaulters that are actually that.

Recall: How many of the actual default profiles does the system correctly identify? Recall refers to the percentage of all the default profiles that the model catches.

F1-Score: Is a combination of precision and recall for a overall behavior grade.

![image](https://github.com/NJAimesD/AIAcademyCS/assets/159951082/415fb249-5fd1-4f27-a33f-350fe19e7c1a)
-the most important for us is Recall, because in this case False Negatives are of high concern,  since we as an institution don't want to give a loan to someone that will default, because the model predicted otherwise. We'd would be losing money.
So for us is more important to predict loan declines correctly than approvals.
According to those metric, the best model is the Random Forest Classifier.  

<img src="https://github.com/NJAimesD/AIAcademyCS/assets/159951082/d0a201e2-b9af-40b5-bc33-01879c295d7e" width="600" /> 
Finaly, we compare the ROC Curves of each model, that tell us how good the classifier is, catching the correct values, while avoiding mistakes.



### Optimal model: Random Forest:
The Random Forest Classifier is a model based in Decision Trees, which is an algorithm that breaks down complex problems into simple steps, and based on input features, calculates the best route to predict the best answer.  
Random Forest combines multiple decision tree and averages their outcomes, to provide an accurate overall answer.


For the Random Forest Classifier, we got:
Precision = 0.941  
Recall = 0.939  
F1 Score = 0.94  




#### ROC Curve
The arean under the Curve is very close to 1, about 0.95, so our model is catching most of the correct values, while avoiding mistakes.


<img src="ttps://github.com/NJAimesD/AIAcademyCS/assets/159951082/dbcec821-d13c-4e77-893f-9e5e0bfb5f32" width="700" /> 


#### Confusion Matrix

We can clearly see that the results are well predicted, so, far most of the actual default values were predicted as so, as well as the non default ones.

<img src="https://github.com/NJAimesD/AIAcademyCS/assets/159951082/01096403-d402-4357-8b1f-e48b8c65accc" width="700" /> 





