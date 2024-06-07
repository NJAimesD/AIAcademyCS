# Credit Risk Crystal Ball: Predicting Risk with Machine Learning
![image](https://github.com/NJAimesD/AIAcademyCS/assets/159951082/9249a348-f7f3-46e8-bca0-742d921947ce)

### Overview and Business Understanding

Credit risk prediction is a cricial process for financial institutions, aiming to asses the likehood of a borrower defaulting on a loan. That way the non-defaulter people can access easily to credist with better
conditions, while the institutions reduce the risk of finantial loss.
There are many techniques to predict credit risk, but Machine Learning can be used to automate the prediction process, since it learns the patterns asociated with a defaulter profile and its use reduces time and resources consumption.
Detecting people with a high risk profile can be a complex task, but still it implies better profit margin for the institution, and ML using improves a lot the efficiency, and the institution resources can be now used in other areas that require human supervision.

Our team at Deloitte seeks to use different machine learning models to predict the credit risk for different profiles, test them and implement a metric to compare them, once evaluated, we´ll select the model with the best results, as well as understand what are the features with the greatest impact in the final result, that will give added value to the client.   
#### Benefits
* A streamlined process for approving loans.
* Higher accuracy in the approval process.
* Higher client satisfaction.
* Loan approval fairness, reducing biases

![image](https://github.com/NJAimesD/AIAcademyCS/assets/159951082/aceb230e-da3f-4f34-abf0-20d5d68b645a)

### Description of Data


**Data Source**: Credit Risk Dataset: (https://www.kaggle.com/datasets/laotse/credit-risk-dataset)

**Exploratory analysis**   
We first reviewed all the variables to understand their meaning.
![image](https://github.com/NJAimesD/AIAcademyCS/assets/159951082/4d96d12d-fde1-47ea-8751-e23fe36e0add)

The target variable in this dataset is loan status There are 11 independent variables used for modeling, with a range of 32,581 to 28,638 non-null values. The average age of the sample population is 27 years old, with an average loan amount of around $10,000 and an average credit history of 5.8 years.

The target variable in this case, with 78.3% of values indicating non-default and 21.7% indicating default, is significantly unbalanced, a data balancing technique was needed, specifically, SMOTE, that is an oversampling technique used to balance the class distribution of a dataset by creating synthetic minority class samples..
![image](https://github.com/NJAimesD/AIAcademyCapstone/assets/159951082/0d3f2174-0525-43d2-af43-126b4d85363d)

A comparative visual analysis was performed, where we built a correlation matrix for all the variables, 
![image](https://github.com/NJAimesD/AIAcademyCapstone/assets/159951082/5355d94d-3a12-4858-8514-f387efed3549)

Checking the variables correlations to the Loan Status, we found that the most correlated variables are  Loan Percent Income, Loan Interest Rate as well as the Loan Grade D, so we would expect this variables to have the greatest impact on the final result.

![image](https://github.com/NJAimesD/AIAcademyCapstone/assets/159951082/209974dc-5a84-42a7-9adb-3165658c9af1)





Correlation matrix


### Data Understanding and Analysis
