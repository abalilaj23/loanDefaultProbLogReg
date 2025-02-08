                                                Predict Loan Default With Logistic Regression
        
        Introduction
        
As a consultant specializing in predictive analytics, Bank X engaged me to address a pressing business need in the loan division. The bank's goal is to enhance the accuracy of loan repayment predictions and, by so doing, minimize the risk of defaults. The task assigned to me as the consultant was to develop a robust predictive model that can provide actionable recommendations that can aid in better decision-making and improve the bank's financial outcomes.  

I developed a logistic regression (logit) predictive model to address this need. A logistic regression is known for its effectiveness in addressing binary classification problems. As such, it is a good model for predicting the probability that a data point falls into a specific category, in this case, default or repay. The model at hand was trained on historical loan data collected by the bank from the individuals whose loans had previously been approved. This data includes a variety of factors such as borrower’s installment amount, annual income, FICO score, revolving balance, past loan inquiries, and credit record. The model estimates the probability of each borrower repaying their loan by analyzing these variables. Moreover, this model allows for understanding how different factors influence loan repayment probabilities.

          Dataset Description

This model uses a dataset with more than 9500 historical observations to predict the probability of loan default (variable default: 1 = default, 0= no default) based on 6 independent variables. The independent variables are the following:

Installment: total amount of loan installments to pay per month in $. min = $16; max= $927 ; mean= $344.31;

log_income: income transformed into a log variable to handle skewness. min = 3.3 ; max= 5.85 ; mean= 4.73 ;

fico_score: credit score determined by credit bureaus. min =617; max= 822  ; mean= 697;

rev_balance: the balance carried out from one month to the next in thousand $. min = 0; max= 1207.36 ; mean= 21.23 ;

inquiries: number of credit inqueries in the last year. min = 0; max= 33 ; mean=2.34 ;

records: number of derogatory records like bankruptcy. min = 0; max= 2 ; mean=0.09 ;

          Model Results

The logistic regression results provide insights into the relationships between the dependent variable (default) and the
independent variables (installment, log_income, fico_score, rev_balance, inquiries, records). Here are some key points from the summary:

1- Pseudo R-squared: The Pseudo R-squared value is approximately 0.053 (0.04849), indicating that the model explains about 4.8% of the variation in the dependent variable.

2-Coefficients:

Intercept: The intercept is 8.7231. This is the log-odds of the dependent variable when all independent variables are zero.

installment: For a one-unit installment increase, the default log-odds increase by 0.0012.

log_income: For a one-unit increase in log_income, the log-odds of default decrease by 0.9202.

fico_score: For a one-unit increase in fico_score, the log-odds of default decrease by 0.0095.

rev_balance: For a one-unit increase in rev_balance, the log-odds of default increase by 0.0051.

inquiries: For a one-unit increase in inquiries, the log-odds of default increase by 0.1157.

records: For a one-unit increase in records, the log-odds of default increase by 0.2784.

P-values: All the p-values are less than 0.05, indicating that each coefficient is statistically significant.

3-Likelihood Ratio Test (LLR) p-value: The LLR p-value tests whether the model, including all predictors, is significantly
better than a null model with no predictors. The very low p-value (1.657e-58) suggests that the model is statistically significant.

Overall, the logistic regression model suggests that the included variables have a significant impact on predicting the
likelihood of default.

        Model's Value 

The implementation of the logit regression model offers several key advantages:

Risk Assessment: By assigning a probability loan to each future application, the bank's loan department can identify potential high-risk loans early in the application process, helping the bank minimize potential losses. 

Resource Allocation: The bank can make more efficient resource allocation decisions by accurately predicting repayment probability. For instance, marketing campaigns can focus on high-repayment potential borrowers. 

To Conclude, this predictive model can considerably enhance the efficiency and financial performance of the loan division. The bank can use this model to reduce default rates and improve resource allocation. 






