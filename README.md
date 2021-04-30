# credit-analysis
Using customer credit data collected over the past 6 months, build a model to determine whether a customer will default on a credit loan.

Premise: Over the past year, CreditOne has seen an increase in the number of customers defaulting on loans. Given credit data from customers for the past 6 months, we are to determine whether there is a specific amount that someone should be allowed, or at least whether someone should be approved or not.

Data: Data was queried from a MySQL database and contains the following information -- 
- "default": indicating whether or not a client defaulted on their loan
- "limit_bal": indicating the amount of credit for the individual
- "sex": indicating whether the client is male or female
- "education": indicating the education level of the client (grad school, university, high school, other)
- "marriage": indicating the clients marital status (single, married, divorced, other)
- "age": indicating the clients age
- "pay_1 - pay_6": indicating the history of past payment statys for each month (from April to Sept 2005). For example, pay_1 is for Sept, pay_2 for Aug, etc. Measurements for repayment status include: -2 No Consumption, -1 Paid in Full, 0 Revolving credit, 1 Payment Delay for 1 month, 2 Payment Delay for 2 month, etc.
- "bill_amt1 - bill_amt6": indicating the amount of the bill statement for each month (for April to Sept 2005, as above)
- "pay_amt1 - pay_amt6": indicating the amount of previous payment (from April to Sept 2005, as above)

Task 1: Involves importing the data using SQL. Data is turned into .csv format and cleaned for use in the next task.

Task 2: A thorough exploratory data analysis was conducted.

Task 3: Modeling. Initially, three different regression models were tested (Random Forest Regressor, Linear Regression, and Support Vector Regression) to determine whether limit_bal can be predicted. Results were not good, so limit_bal was discretized and predictions were attempted using a classification method. Then, a decision tree classifier was also used to predict whether a client would default or not.  

Ultimately, predicting the amount of credit a client should be allowed (limit_bal) was not possible with the given data. However, predicting whether or not a client would default was possible, and depended largely on the clients payment status and whether they were behind on their payments.
