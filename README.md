# starbucks_capstone
Udacity capstone project to evaluate Starbucks promotion offers.

### Motivation:
The Starbucks capstone project is the final project in my data science nano degree at Udacity.  In this project I clean, model, and analyze simulated Starbucks mobile app data concerning offer promotions.  I use this opportunity to showcase the skill I have gained thus far.  My main goals are to create a model that will predict the success of promotion, predict individual net transactions(transaction amount - offer reward), and determine relationships between users, offers, and net transaction amounts.    


### Libraries used:
Pandas, numpy, math, json, matplotlib.pyplot, re, random, datetime, sklearn, scipy, and statsmodels.api.


### Files:
- data: Contains three data Files.  All data is simulated data from Starbucks.
  - portfolio.json: Data about offer promotions
  - profile.json: Demographic data about users profile
  - transcript.json: All offer and transaction interactions.
- pic1.png: image file used in introduction of Starbucks_Capstone_notebook.IPYNB
- pic2.png: image file used in introduction of Starbucks_Capstone_notebook.IPYNB
- Starbucks_Capstone_notebook.IPYNB: Work notebook covering data cleaning, modeling, and analysis.
- Starbucks_Capstone_notebook.htm: HTML version of Starbucks_Capstone_notebook.IPYNB

## Summary

- Modeling net transactions preformed poorly for predicting individual interactions(highest R squared = 0.109), but modeling correctly predicted the overall success of multiple or individual promotions within 0.3% to 8.6% difference of the actual.
- Modeling offers completed created a good model that can be used in making recommendations.  The model has an F1 score of 0.72.
- Consistent significant modeling predictors(P < 0.05) were female, income, days_as_member, and duration.
- Higher duration and difficulty offers had higher participation.
- Females have a higher average net transaction while having a similar number of offers completed to males.
- Discount offers have a higher average net transaction while having a similar number of offers completed to BOGO offers.
- Higher income individuals have a higher probability to have a higher net transaction.
- Offer participation for age, income, and days as a member mirror their population distributions.


#### Challanges

- Vectorizing tasks: There are a number of tasks that use for loops to impute age or income.  For loops cause them to take more time to complete.  If we can vectorize these tasks we would significantly reduce the time it would take to run tasks.
- Pulling dictionary values from a column.  In the transcript data frame, the value column contains a dictionary.  There were three different objects(offer id, reward, and amount).  I used for loops to pull the values out of the dictionary.  If there is a way to vectorize this it would dramatically reduce the time it take to run the task.
- Missing data: Age = 118, null gender, and null income values were all missing data.  I chose not to discard them because they made up over 10% of the data.  I imputed the gender as unknown and in the end it showed that this group had very few interactions when compared to males and females.  
###### Author
Ryan Mezera
