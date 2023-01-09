# Bank-Effectiveness-Prediction
**Project Title : Predicting the effectiveness of bank marketing campaigns**

**Problem Description**

The data is related with direct marketing campaigns (phone calls) of a Portuguese banking institution. The marketing campaigns were based on phone calls. Often, more than one contact to the same client was required, in order to access if the product (bank term deposit) would be ('yes') or not ('no') subscribed. The classification goal is to predict if the client will subscribe a term deposit (variable y).

**Data Description**

**Input variables:**

Bank Client data:

age (numeric)

job : type of job (categorical: 'admin.','blue-collar','entrepreneur','housemaid','management','retired','self-employed','services','student','technician','unemployed','unknown')

marital : marital status (categorical: 'divorced','married','single','unknown'; note: 'divorced' means divorced or widowed)

education (categorical: 'basic.4y','basic.6y','basic.9y','high.school','illiterate','professional.course','university.degree','unknown')
default: has credit in default? (categorical: 'no','yes','unknown')

housing: has housing loan? (categorical: 'no','yes','unknown')

loan: has personal loan? (categorical: 'no','yes','unknown')
Related with the last contact of the current campaign:

contact: contact communication type (categorical: 'cellular','telephone')

month: last contact month of year (categorical: 'jan', 'feb', 'mar', ..., 'nov', 'dec')

day_of_week: last contact day of the week (categorical: 'mon','tue','wed','thu','fri')

duration: last contact duration, in seconds (numeric). Important note: this attribute highly affects the output target (e.g., if duration=0 then y='no'). Yet, the duration is not known before a call is performed. Also, after the end of the call y is obviously known. Thus, this input should only be included for benchmark purposes and should be discarded if the intention is to have a realistic predictive model.

**Other attributes:**

campaign: number of contacts performed during this campaign and for this client (numeric, includes last contact)

pdays: number of days that passed by after the client was last contacted from a previous campaign (numeric; 999 means client was not previously contacted)

previous: number of contacts performed before this campaign and for this client (numeric)

poutcome: outcome of the previous marketing campaign (categorical: 'failure','nonexistent','success')

**Output variable (desired target):**

y - has the client subscribed a term deposit? (binary: 'yes','no')

**Summary of the project**

Data Visualization: 

Data visualization techniques for instance histogram, line graphs, heatmaps, box plots,pie charts etc helps us in understanding the pattern the data follows. Firstly, we used a pie chart plot to look at the target variable - ‘Term Deposit’. Then we used bar plots and boxplots to visualize the other variables, as most of the variables are categorical in nature. Further we went on to look at the age and job type distribution with respect to Term Deposit.
Feature Engineering:  
Feature engineering is a method of converting raw data into desirable features before fitting it into a machine learning model which results in better performance. We used feature engineering techniques like One Hot encoding and Label Encoder. Additionally we dropped columns whose most of the values were unknown. 

Feature Selection:-

Feature selection helps in reducing the number of input variables to decrease the computational cost of modeling and in some cases it improves the performance of the model.As the number of input variables were not excessive  and all of them were significant, we choose all the features for the machine learning algorithm.

Model Evaluation metrics :- 

We Evaluated the model on different metrics which helps us to better optimize the performance, fine-tune it, and obtain a better result. And got the results from the best suitable model for our project. Following are the evaluation metrics for our selected model:-
Confusion matrix :- A confusion matrix is defined as the table that is often used to describe the performance of a classification model on a set of the test data for which the true values are known.
Accuracy :- Accuracy simply measures how often the classifier correctly predicts.
Precision :-Precision explains how many of the correctly predicted cases actually turned out to be positive.the precision score calculated for our model as 0.9187 
 Recall (Sensitivity) :- Recall explains how many of the actual positive cases we were able to predict correctly with our model.The Recall score calculated for our model as 0.9268
F1 Score :-  It gives a combined idea about Precision and Recall metrics. The  F1 score calculated for our model is  0.9227
 Receiver Operator Characteristic (ROC)
Area Under the Curve (AUC) 

Model Selection:-

After training the dataset on nine  models and evaluating on the five evaluation metrics, the Gradient Boosting Classifier model came out to be the best model with an F1 score of  0.92 and matthews_corrcoef of 0.84.
Gradient boosting does not penalize missed-classified cases but uses a loss function instead. Loss function can be the mean average error for log loss for classification problems. In addition, the gradient boosting algorithm uses the gradient descent method to continuously minimize the loss function to find the optimal point.


