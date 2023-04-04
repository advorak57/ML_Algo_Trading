# ML_Algo_Trading
## Results:


This project aims to develop a trading algorithm for emerging markets stocks by applying machine learning techniques. We utilized historical OHLCV data and implemented a support vector machine (SVM) classifier as the initial model. The algorithm generates buy and sell signals based on simple moving average (SMA) crossovers, and we compared the returns of our trading strategy to the actual returns of the market.

### Methodology
We imported the necessary libraries and loaded the OHLCV dataset into a pandas DataFrame.
We filtered the dataset to only include closing prices and calculated the daily returns.
We computed short-term and long-term simple moving averages (SMA) for the closing prices.
We created trading signals based on the daily returns, with a buy signal (1) for positive returns and a sell signal (-1) for negative returns.
We calculated the strategy returns by multiplying the actual returns with the shifted trading signals.
We prepared the dataset for machine learning by splitting it into training and testing sets and scaling the input features.

We trained an SVM classifier using the training dataset and evaluated its performance using the testing dataset.
We tuned the SVM model by adjusting the size of the training dataset and the SMA input features, aiming to improve the trading algorithm's returns.
We implemented an alternative machine learning classifier (AdaBoost) and compared its performance to the original SVM model and the tuned trading algorithm.


### Results and Observations
After evaluating the performance of the SVM model and the alternative AdaBoost classifier, we observed the following:

The SVM model's performance could be improved by adjusting the size of the training dataset and the SMA input features. The best set of parameters was found through experimentation and comparison of the cumulative returns of the trading strategies.
The alternative AdaBoost classifier performed differently compared to the SVM model. By comparing the classification reports and the cumulative returns plots, we could determine which model performed better in terms of accuracy, precision, recall, F1-score, and overall returns.

### Conclusions

Based on the classification reports for each of the changes I made to the algorithm, increasing the size of the training data set from 3 to 6 months improved the accuracy by 1%. 

Expanding the windows of the SMA from 6 and 100 to 10 and 150 dropped accuracy by 1%. 

Review saved classification reports for additional data. 

I ran the AdaBoosterClassifier as an additional model. This did not perform better than SVC. Accuracy was down another percent and recall was lower in finding buy signals. It was better at finding sell signals slightly.