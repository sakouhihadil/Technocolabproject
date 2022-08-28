# Technocolabproject
# Prosper Loan Risk Prediction 

We have a raw data collected from the bank 

So, in this project we will analyse this data and predict there will be low risk or high risk while giving the loan.

## Understanding the Dataset

- The data provided contains the information of the borrower requiring loan.

- Total data comprises of 113937 rows × 86 columns

- There are many features present in the data some of that will be useful for us based on which we will make our predictions.

## Cleaning the data

- First, we did the data cleaning that is removing all the null values present in the data.

- Did a quick check on the datatypes and number of columns required us.

## EDA

- First of all we will do the pre-processing of the data.

- Replace all the NAN values with 0.

Select a dataset d1 that will support our task of into performance of the loan.

- Here are some features that we used in our dataset:

IncomeRange,CreditGrade,ProsperScore,IsBorrowerHomeowner,ProsperRating (Alpha),Investors, EstimatedReturn.



# Data visualization

- Based on few features we checked many possibilities of the come that would come under us.

- For e.g. we checked if Borrower are Homeowner.

and we came to the conclusion that the feature of owning a home alone, does not affect the performance of the loan performance.

- We also checked for the Incomerannge of the borrower and we get to know that most borrowers have an income of 25k-50K and 50K-75K.So it looks like the income feature does affect the loan performance.

- Just like this we did the data visualization for many more factors.

- And all together if implies that having a better credit score, being a homeowner, having an estimated return of 0-20% or having a dept to income ratio of 0-25% will always have more chances of getting you more investors , resulting in a better loan performance.


# Univariate Analysis

- Plotted histogram to see the distribution of data for each column and found that few variables are normally distributed. However, we can't really say about  that which variable needed to be studied.

## Model Building

# Metrics considered for Model Evaluation

- Accuracy: What proportion of actual positives and negatives is correctly classified?

- Precision: What proportion of predicted positives are truly positive ?

- Recall: What proportion of actual positives is correctly classified ?

# Logistic Regression

- Logistic Regression helps find how probabilities are changed with actions.

- Logistic regression involves finding the best fit S-curve where A is the intercept and B is the regression coefficient. The output of logistic regression is a probability score.



# Naive Bayes

- It is mainly used in text classification that includes a high-dimensional training dataset.

- It is a probabilistic classifier, which means it predicts on the basis of the probability of an object.

# Decision Tree

- used for both classification and Regression problems, but mostly it is preferred for solving Classification problems.

- This algorithm compares the values of root attribute with the record (real dataset) attribute and, based on the comparison, follows the branch and jumps to the next node.



# Choosing the features

After choosing Decision Tree model based on confusion matrix here where \*\*choose the features\*\* taking in consideration the deployment phase.

- We know from the EDA that all the features are highly correlated and almost follows the same trend among the time.

When we apply the \*\*logistic regression\*\* model the accuracy was 90%.

When we apply \*\*naive bayes\*\* model the accuracy was 87%.

When we apply \*\*decision tree\*\* the accuracy was 91%

As decision tree model has 91% accuracy, we decided to go with decision tree model for deployment.

## Deployment

- We reduced the number of features to 9 using feature importance.

- Using pickle library we put the model in a .pkl file which we imported in the app.py file.

# Flask

- To prepare the app.py file we used flask library as an intermediary between the form page and the model in the pkl file 

- We imported the pkl model file and we used the information provided by the user in the form page to predict his loan eligibility than display the result in the top of the form (html )page.

# Web Page

- We prepared a basic html form page where the user has to fill the 9 features in order to get his loan risk prediction.

# Heroku

- We deployed our app to heroku. In this way, we can share our app on the internet with others. 
