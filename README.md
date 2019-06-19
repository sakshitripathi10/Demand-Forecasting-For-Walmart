# Demand-Forecasting-For-Walmart
The project involves prediction of accurate sales for 45 stores of Walmart, one of the US-based leading retail stores, considering the impact of promotional markdown events. Checking if macroeconomic factors like CPI, unemployment rate, etc. have an impact on weekly sales 
# Details of data :-
This project consist of three data files -> Features,Stores and Train which are in total of more than 400k rows of data.
# Features :-
'Store'(number of stores), 'Date', 'Temperature', 'Fuel_Price', 'MarkDown'(five columns),'CPI'(consumer price index), 'Unemployment' and a  'IsHoliday'(boolean containing whether the week has holidays or not).
# Stores :-
'Store'(number of stores), 'Type'(type of the store) and 'Size'.
# Train :-
'Store'(number of stores), 'Dept'(departments),'Date', 'Weekly_Sales', 'IsHoliday'(boolean containing whether the week has holidays or not).
# Algorithms applied on the data :-
As the goal of this project was to forecast the sales of the walmart , therefore there were three algorithms applied on the data -> Linear Regression , Decision Tree Regressor, Random Forest Regressor .
# Linear Regression :-
 linear regression is a linear approach to modeling the relationship between a scalar response (or dependent variable) and one or more explanatory variables (or independent variables). The case of one explanatory variable is called simple linear regression. In linear regression, the relationships are modeled using linear predictor functions whose unknown model parameters are estimated from the data. Such models are called linear models.[3] Most commonly, the conditional mean of the response given the values of the explanatory variables (or predictors) is assumed to be an affine function of those values; less commonly, the conditional median or some other quantile is used.Since our goal was to estimate weekly sales based on features provided to us, Linear Regression sounded like a good fit. Linear regression models the relationship between a scalar variable and a set of independent variables. Using the merged dataset which matched all stores to their specific features, and the yielded predictive model would tell us which features were most important to predicting weekly sales. The predictive model showed that the most important feature in determining weekly sales was the ‘IsHoliday’ feature. This means that the weeks that contained a holiday were the most successful when it came to weekly sales, while the least important feature was temperature. The dates that were taken into account contained important days such as the Super Bowl, Labor Day, Thanksgiving (most likely including Black Friday and Cyber Monday), and Christmas.
# Decision Tree Regressor :-
Decision Tree is a decision-making tool that uses a flowchart-like tree structure or is a model of decisions and all of their possible results, including outcomes, input costs and utility.Decision Tree is a decision-making tool that uses a flowchart-like tree structure or is a model of decisions and all of their possible results, including outcomes, input costs and utility.
#  Random Forest Regressor :-
A random forest is a meta estimator that fits a number of classifying decision trees on various sub-samples of the dataset and uses averaging to improve the predictive accuracy and control over-fitting.Considering that our project goal was to predict sales forecasting from a weekly basis, I decided to use RandomForestRegressor. One of the biggest benefits of using the random forest is that when you use enough trees for predictions overfitting will not be an issue, however using too many trees can drastically affect the time it takes for the algorithm to run completely. Another benefit of using random forest was that it provided good results without necessitating too much parameter adjustments. In fact, the only parameter I adjusted for this portion was the n_estimators, which is the number of trees the algorithm builds to perform the necessary prediction. I ran the algorithm with various n_estimators num_est = [2,4,10,20,30,40,50,60,70,80,90,100] to which I compared the resulting accuracy score to see which number of trees would best fit the dataset we were using. After running the algorithm through all 12 of the n_estimators, I found that the “60” gave the highest accuracy score, indicating that it was the most suitable value to use for n_estimators for the algorithm.
# Conclusion :-
The best machine learning algorithm apllied on this data to get accurate prediction was Random Forest Regressor.
