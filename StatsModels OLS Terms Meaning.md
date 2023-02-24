Refer this for more details: http://work.thaslwanter.at/Stats/html/statsModels.html
### Important assumptions for OLS:
1. Sample data is independently & identically distributed (IID)
2. Residuals are independently & identically distributed (IID) random normal variables. There is no autocorrelation in residuals.
3. Population mean of residuals(errors) is zero.
4. The residuals(error) have a constant variance means homoscedasticity (no heteroscedasticity)
5. The regression model is linear in the coefficients and the error term.
6. Large outliers are unlikely

### Meaning of terms in OLS results:

1. <b>R Squared:</b>  
    <b> It answers:</b> What percentage of variation is explained by the regression line?  
    Explains percentage of variation in y(dependent variable) by x(independent variable or variables or regressors)
   - if R=0.80, 80% of variation in y is explained by x, & remaining 20% are random. So higher value is better.
   

2. <b>Adj. R-squared:</b>   
    <b> It answers:</b> Does addtional regressor variables improves R Squared? means improves & explains variation in y, regression line.


3. <b>F-Statistic:</b>  
    It is a ratio of two quantities that are expected to be roughly equal under the null hypothesis, which produces an F-statistic of approximately 1. Measures if residuals have constant variance, means homoscedasticity & no heteroscedasticity.


4. <b>Prob (F-Statistic):</b>    
    <b> It answers:</b> Based on F-statistic, if the fit of your model is equal to intercept-only model? That is, all of the regression coefficients are zero. 
    Regression models without predictors are also known as intercept only models
     - Null hypothesis: The fit of the intercept-only model and your model are equal.  
     - Alternative hypothesis: The fit of the intercept-only model is significantly reduced compared to your model.


5. <b>Log-Likelihood:</b>  
    <b> It answers:</b> Goodness of fit for the model. Higher the value, better is the model. It is the sum of the natural log of conditional probabilities. maximizes the log-likelihood of the observed sample. Likelihood gives best values for a model we select or assume the sample data is following


6. <b>AIC(Akaike Information Criterion)</b>  
    <b> It answers:</b>  
    The model with lowest AIC value is selected. 

7. <b>BIC(Bayesian Information Criterion)</b>  
    <b> It answers:</b>  
    The model with lowest BIC value is selected
    

<b>Following 6 to 12 are tests on residual errors data. These checks validity of OLS assumptions on residuals:  

- If residuals follow Independent & identically distributed (iid) random normal variables pattern.  
- If there is no autocorrelation in residuals.

6. <b>Omnibus (Residuals):</b>  
     D’Agostino-Pearson Omnibus Test 
    <b> It answers:</b> Skewness & Kurtosis of residuals. Lesser the value, better is the model. Near to zero means random normal distribution of residuals, which is one of the assumptions for OLS. stats.normaltest(x)


7. <b>Prob(Omnibus) (Residuals):</b>  
   <b> It answers:</b> Hyothesis test of normal distribution of residuals based on Omnibus value. Closer to 1, means normal distribution. stats.normaltest(x)
      - Null Hypothesis: Residuals follow normal distribution  
      - Alternate Hypothesis: Residents don't follow normal distribution.


8. <b>Durbin-Watson (Residuals):</b>  
    <b> It answers:</b> autocorrelation of residuals.   
    - Ranges from 0-4. Ranges from 1.5-2.14 are accepted.
    - 2-> Normal Random Distribution, 0-2->Positive autocorrelation, 2-4->Negative autocorrelation of residuals


9. <b>Jarque-Bera (JB) (Residuals):</b>  
    <b> It answers:</b> Matches omnibus test. Larger value means residual errors are not normal distributed


10. <b>Prob(JB) (Residuals):</b>  
    <b> It answers:</b> Hyothesis test for JB.


11. Skew (Residuals):  
    <b> It answers:</b> Positive value->Right skewed. Negative value->Left skewed


12. <b>Kurtosis (Residual):</b>  
    Please note it is 'Excess Kurtosis', 3 + Kurtosis. Execss Kurtosis is measured with respect to Standard Normal Distribution Kurtosis, which has value of 3.  
    <b> It answers:</b> Postive value->Heavy tail(more data in tail). Negative value->Light tail(little data in tail)