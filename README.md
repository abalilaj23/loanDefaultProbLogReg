# Predict Loan Default With Logistic Regression

## Introduction

As a consultant specializing in predictive analytics, Bank X engaged me to address a pressing business need in the loan division. The bank's goal is to enhance the accuracy of loan repayment predictions and, by doing so, minimize the risk of defaults. The task assigned to me as the consultant was to develop a robust predictive model that can provide actionable recommendations to aid in better decision-making and improve the bank's financial outcomes.  

I developed a **logistic regression (logit)** predictive model to address this need. Logistic regression is known for its effectiveness in addressing binary classification problems, making it an ideal model for predicting the probability that a data point falls into a specific category— in this case, default or repay. The model was trained on historical loan data collected by the bank from individuals whose loans had previously been approved. This data includes a variety of factors such as the borrower’s installment amount, annual income, FICO score, revolving balance, past loan inquiries, and credit record. The model estimates the probability of each borrower repaying their loan by analyzing these variables. Moreover, this model allows for understanding how different factors influence loan repayment probabilities.

## Dataset Description

This model uses a dataset with more than 9,500 historical observations to predict the probability of loan default (variable: `default`—1 = default, 0 = no default) based on 6 independent variables. The independent variables are as follows:

- **Installment**: Total amount of loan installments to pay per month in dollars.  
  - Min: $16  
  - Max: $927  
  - Mean: $344.31

- **log_income**: Log-transformed income to handle skewness.  
  - Min: 3.3  
  - Max: 5.85  
  - Mean: 4.73

- **fico_score**: Credit score determined by credit bureaus.  
  - Min: 617  
  - Max: 822  
  - Mean: 697

- **rev_balance**: Revolving balance carried out from one month to the next (in thousands of dollars).  
  - Min: 0  
  - Max: 1207.36  
  - Mean: 21.23

- **inquiries**: Number of credit inquiries in the last year.  
  - Min: 0  
  - Max: 33  
  - Mean: 2.34

- **records**: Number of derogatory records like bankruptcy.  
  - Min: 0  
  - Max: 2  
  - Mean: 0.09

## Model Results

The logistic regression results provide insights into the relationships between the dependent variable (`default`) and the independent variables (installment, log_income, fico_score, rev_balance, inquiries, and records). Here are some key points from the summary:

1. **Pseudo R-squared**: The pseudo R-squared value is approximately 0.053, indicating that the model explains about 4.8% of the variation in the dependent variable.

2. **Coefficients**:
   - **Intercept**: 8.7231 (log-odds of default when all independent variables are zero).
   - **installment**: For each $1 increase in the installment, the default log-odds increase by 0.0012.
   - **log_income**: For each 1-unit increase in log_income, the log-odds of default decrease by 0.9202.
   - **fico_score**: For each 1-unit increase in fico_score, the log-odds of default decrease by 0.0095.
   - **rev_balance**: For each $1,000 increase in the revolving balance, the log-odds of default increase by 0.0051.
   - **inquiries**: For each additional inquiry, the log-odds of default increase by 0.1157.
   - **records**: For each additional derogatory record, the log-odds of default increase by 0.2784.

3. **P-values**: All p-values are less than 0.05, indicating that each coefficient is statistically significant.

4. **Likelihood Ratio Test (LLR) p-value**: The very low p-value (1.657e-58) suggests that the model is statistically significant and is significantly better than a null model with no predictors.

## Model's Value

The implementation of the logistic regression model offers several key advantages:

- **Risk Assessment**: By assigning a probability to each future loan application, the bank's loan department can identify potential high-risk loans early in the application process, helping minimize potential losses. 

- **Resource Allocation**: The bank can make more efficient resource allocation decisions by accurately predicting repayment probabilities. For instance, marketing campaigns can focus on borrowers with higher repayment potential.

## Conclusion

This predictive model can considerably enhance the efficiency and financial performance of the loan division. By using this model, the bank can reduce default rates, improve resource allocation, and make data-driven decisions to enhance its operations.





