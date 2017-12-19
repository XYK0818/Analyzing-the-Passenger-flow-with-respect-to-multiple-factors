# Analyzing the Passenger flow with respect to multiple factors
For this site, we are going to analyze the flow of passenger givn some factors. The data set contains the factors such as barometric pressure, wind speed, temperature, daytime, day of the week and the indicidence of fog etc. among with the volumn of passengers flow through some units or stations.

## Linear regression
We selected the following features for the model and convert the data by appling ‘pd.get_dummies’ methods for regression to compute the coefficients and to make predictions for number of passengers per hour. 
• “day_week”: whether the day was a weekday
• “hour”: time of day
• “station”: train over a bunch of stations
• “conditions”: the weather conditions
• “fog”: whether it’s fog
• “meantemp”: the temperature of that time

We use residual error to show how well the model fit the data. Usually, the residual closer to normal distribution means the fitting result is better. As we can see, the regression using sm is more like a normal distribution.
Rss is used to measure how close the data can be fitted to regression line.As for OLS using Statsmodel, the rss is about 42% and it’s quite stable. So the regression model can be used to predict the passenger flow. As for the SGDregressor module from sklearn, the linear regression model explains about 40% of the variability of the Entries_num_hourly variable. And it’s varies when we apply this model a few times. It would not be a good enough model for creating a precise model to predict passenger flow. It’s more suitable to study the effects of changes in some of the predictor values (e.g. weather, time of day, day of week, etc). The result shows that different linear regression models have different degree of applicability among some specific problems. 

## The histogram 
The histogram is used to plot the distribution of Entries_num_hourly for the sample with and without fog. From this plot it shows that passengers are much more in days with no fog than in days with fog. ​

## Visualize with ggplot
Ggplot is powerful sketch tool for data analyzing. In this site, we check this data by analyzing the relationship between temperature with windspeed. It shows that when temperature goes up, the windspeed dropped.
Then we draw the relation between the number of passengers and the time of the day. It seems that the passengers are more likely to show up from 1 pm to 8pm

## Conclusion
As we can see, various factors can affect the attendance of passengers.
  


