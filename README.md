# Machine Learning Trading Bot

## Establishing the Base Line using SVC Classifier model

1. generated trading signals using long/short-window SMA values
2. trained and made predictions based on test data
3. compared actual returns vs. predicted returns 

![Actual Returns vs. Strategy Returns](https://raw.githubusercontent.com/halamkim/challenge_14/main/baseline%20plot.png)

**Conclusion**: From 2015 - about late 2017, there isn't a noticeable difference between the two. From late 2017 to mid 2018, actual returns performed slightly better than strategy returns. However, from then, the strategy returns greatly surpass the actual returns.

## Changing the Training Data Period 
1. 6 months 
![Actual Returns vs. Strategy Returns(6 months of training)](https://raw.githubusercontent.com/halamkim/challenge_14/main/6month%20training%20data%20plot.png) 


2. 1 month
![Actual Returns vs. Strategy Returns (1 month of training)](https://raw.githubusercontent.com/halamkim/challenge_14/main/1%20month%20training%20data%20plot.png)

**Conclusion**: sing this dataset, starting from the same start date and adjusting the training data period had a significant difference in the results of Actual Returns vs. Strategy Returns. The best strategy return data was from the shortest training data period of 1 month where it outperformed the actual returns throughout. The longer the training data period, the worse the data performed especially between 2019 and 2020. 


## Changing the SMA Input Features
1. short_window = 4, 
long_window = 30

![Returns from short window SMA of 4 and long window of 30](https://raw.githubusercontent.com/halamkim/challenge_14/main/SMA4_30.png)
2. short_window = 4,
long_window = 180
![Returns from short window SMA of 4 and long window of 180](https://raw.githubusercontent.com/halamkim/challenge_14/main/SMA4_180.png)

**Conclusion**: Changing the SMA iniput features had a great influence on the strategy returns. Changing the long_window whether it was shorter or longer than 100 (original) made our results worse. 

## Mixed Parameters for the Best Result
![Best Results SMA winows = 3/100, training window = 1 month](https://raw.githubusercontent.com/halamkim/challenge_14/main/Best%20plot.png)
 
**Conclusion**: The original SMA windows of 4 and 100 worked well and I slightly modified the short window to be 3 but kept it to be similar. The best training window was 1 month so I went back to that. I chose these parameters because the strategy returns are always beating the actual returns consistently which shows less risk. 

## Logistic Regression
![Logistic Regression Plot](https://raw.githubusercontent.com/halamkim/challenge_14/main/Logistic%20Regression%20Plot.png)

**Conclusion**: compared to the baseline model, the logistic regression model performed better from late 2019 to the end of 2020 when the strategy returns underperform the actual returns. 


## Overall Evaluation 
Overall, the best performing plot that was chosen is not beating the actual returns by a lot but rather consistently. It takes trial-and-error to find the best performing strategy. Hwoever, this proves that what defines "best strategy" is customer-oriented since the best strategy might include low risk and always outperforming the actual market just like the one chosen as the best plot in this challenge. 