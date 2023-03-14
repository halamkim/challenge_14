# Machine Learning Trading Bot

## Establishing the Base Line using SVC Classifier model

1. generated trading signals using long/short-window SMA values
2. trained and made predictions based on test data
3. compared actual returns vs. predicted returns 

![Actual Returns vs. Strategy Returns](https://raw.githubusercontent.com/halamkim/challenge_14/main/baseline%20plot.png)

**Conclusion**: From 2015 - about late 2017, there isn't a noticeable difference between the two. From late 2017 to mid 2018, actual returns performed slightly better than strategy returns. However, from then, the strategy returns greatly surpass the actual returns.

## Changing the training data period to be 6 months 
![Actual Returns vs. Strategy Returns(6 months of training)](https://raw.githubusercontent.com/halamkim/challenge_14/main/6month%20training%20data%20plot.png) 

**Conclusion**: From 2015 - mid 2018, both returns seem to be pretty similar. From mid 2018 to the beginning of 2020, strategy performs worse by quite a bit (approximately 10-15%). From the beginning of 2020, the strategy returns exceed the actual returns continuously. 

## Changing the training data period to 1 month
![Actual Returns vs. Strategy Returns (1 month of training)](https://raw.githubusercontent.com/halamkim/challenge_14/main/1%20month%20training%20data%20plot.png)

**Conclusion**: The stategy returns are always performing better given any date. 


### **Impact of different training data periods:** 
Using this dataset, starting from the same start date and adjusting the training data period had a significant difference in the results of Actual Returns vs. Strategy Returns. The best strategy return data was from the shortest training data period of 1 month where it outperformed the actual returns throughout. The longer the training data period, the worse the data performed especially between 2019 and 2020. 