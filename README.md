# Predicting Impressions from Advertisement Expenditures and Advertisement Duration of Political Ads on Snapchat
This repository includes simple and multiple linear regression analyses for Snapchat political ad data.  
## Background ## 
  Throughout the past several years, political campaigns have spent astronomical sums of money on advertising and social media outreach. Most notably, Johns Hopkins University Alum and Former New York City Mayor, Michael Bloomberg, [spent $1 billion on his campaign, of which 70% reportedly went towards advertising.](https://knowledge.wharton.upenn.edu/article/how-social-media-is-shaping-political-campaigns/) Former President Donald Trump spent around [$107 million on Facebook ads](https://abc7.com/presidential-race-campaign-spending-trump-political-ads-biden/7452228/) alone during the 2020 Presidential race, while President Joe Biden spent around [$94 million on Facebook ads](https://abc7.com/presidential-race-campaign-spending-trump-political-ads-biden/7452228/) in the same time frame. Although Facebook and Google have consistently dominated political advertising, rising social media platforms, like Snapchat, [offer access to the ‘Gen Z’ population and a larger audience of young voters.](https://deltalab.research.wesleyan.edu/2020/10/28/presidential-advertising-on-snapchat/) President Biden has already spent around [$3 million on Snapchat advertising](https://deltalab.research.wesleyan.edu/2020/10/28/presidential-advertising-on-snapchat/), in addition to fellow Democratic figures like Former NYC Mayor Bloomberg and Senator Elizabeth Warren. Given these figures, and the rising popularity of social media, we seek to determine whether we can predict the number of impressions (views) using advertising expenditures and advertisement duration in the year 2021 from Snapchat’s public Political Ads data. 
## Business Question ##
  Can we predict the number of impressions (views) for an advertisement on Snapchat based on advertisement expenditures and advertisment duration of political advertisements on Snapchat during the year 2021? 
## Data Source ##
  [Snapchat Political Ads Data](https://www.snap.com/en-US/political-ads)
  Snapchat publishes their political advertising data for each year and includes comprehensive information for each political advertisement on their platform. The data file includes basic information for each advertisement transaction such as a unique ID, the currency of the transaction, the cost of the advertisement, the start and end dates for the advertisement, the organization being advertised, and the paying advertiser. The file also includes demographic information such as age brackets, gender, geographic location, target radius, and advertising language. All transactions do not include comprehensive demographic information however every transaction does include the basic information. For the purposes of this analysis, advertisements with no specified end-date (on-going advertisements) were given end-dates of March 2, 2021 because the data was downloaded on March 2, 2021 and the analysis was performed on data that was present at this time. The data was kept in the analysis because the on-going advertisement data reflected the amount spent and the impressions generated thus far, and increased the sample size of the analysis.  
## Data Analysis and Visualizations ## 
### Simple Linear Regression ###
  Simple linear regression was performed to examine the relationship between advertisement expenditures and impressions (graph 1), and advertisement duration (graph 2) and impressions. Linear regression shows the potential relationship between an independent and dependent variable, and in this analysis it showed how the dependent variable, impressions, changed with each dependent variable. Graph 1 ![alt text](https://github.com/apate139/Snapchat-Political-Ads-Linear-Regression/blob/main/MP2%20IvsAE.png) shows how impressions increase as expenditures increase and indicates an R^2 value of 0.9566, which means the percentage of the data points that fit the regression model, in this case 95.66% which indicates the model is a good predictor for this relationship. ![alt text](https://github.com/apate139/Snapchat-Political-Ads-Linear-Regression/blob/main/MP2%20IvsAD.png) Graph 2 shows how impressions change as advertisement duration changes and indicates an R^2 value of 0.0085, which means that .85% of the data points fit the regression model, which indicates the regression model is not a good predictor for this relationship. 
### Multiple Linear Regression ### 
  Mulitple linear regression was performed to examine the potential relationship between advertisement expenditures, advertisement duration, and impressions, however multiple linear regression cannot be shown graphically so no visualization was developed. Multiple linear regression shows the potential relationship between mulitple independent variables and a dependent variable. 
## Findings ##
  The simple linear regression for advertisement expenditures (AE) and impressions had an R^2 value of 0.9566, which means 95.66% of the data can be predicted by the regression model. It had a p-value that was < 0.05, which allows us to reject the null hypothesis, that there is no relationship between AE and impressions, and conclude that there is evidence for some association between AE and impressions. The simple linear regression for advertisement duration (AD) and impressions had an R^2 value of 0.0085, which means that 0.85% of the data can be predicted by the regression model. The p-value was > 0.05, which means we fail to reject the null hypothesis, that there is no relationship between AD and impressions, and do not have sufficient evidence that an association exists between AD and impressions. 
  For the multiple linear regression, the R^2 value was 0.9566, however given that we are working with two independent variables, this value is more complex to interpret. The p-value for AD was 0.7435, which means we fail to reject the null hypothesis. The p-value for AE was found to be 0, due to the value being rounded to 0, which is > 0.05 and indicates that we reject the null hypothesis. The total observations for this regression model were 790, which is a large and shows our model is robust. The final interpretation of this model is: when we control for duration of advertisement, a one-unit difference in advertisement expenditure is associated with a 303.88684 increase in impressions. The equation yielded from this model is: y= -51992.873x -179.24531(duration of advertisement) +303.88684(advertising expenditure)
  These findings indicate that there is a relationship between AE and impressions which is important to Snapchat because it shows their service is successful. Their promise to consumers is fair in that advertising costs lead to impressions and given the high R^2 value found for the association between AE and impressions, the model is a good predictor for the data. This information should be used to guide pricing options, for both Snapchat and consumers, based on predicted impressions from costs. It would be aided by additional data describing successful bids. Bids are end goals specified by advertisers, and given what we know about expenditures and impressions (views), consumers may be persuaded by data analysis showing the association between expenditures and successful bids rather than just views. Clarifying this relationship can help Snapchat increase advertising revenue and aid political campaigns with using resources more efficiently as bids would offer more value for their money instead of just views.  



