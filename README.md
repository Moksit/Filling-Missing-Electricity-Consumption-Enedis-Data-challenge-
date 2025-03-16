# Filling-Missing-Electricity-Consumption-by-Enedis-Data-challenge
The goal is to predict the missing value of electricity consumption of 1000 users. The training data consists of the consumption (with no missing data) of 50000 users on the same period of time.

1- Cleaning: we first fill the holed_ columns of the train data with the information present in y_train. We then remove columns that has missing values. We then devide the X_test into two data files. The first one contains the history of electricity consumption, the second one contains the test data.

The dat challenge website: https://challengedata.ens.fr/participants/challenges/160/
