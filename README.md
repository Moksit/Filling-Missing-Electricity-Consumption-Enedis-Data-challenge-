# Filling-Missing-Electricity-Consumption-by-Enedis-Data-challenge
The data challenge website: https://challengedata.ens.fr/participants/challenges/160/

The goal is to predict the missing value of electricity consumption of 1000 users. The training data consists of a complete consumption history of 50000 users on the same period of time.

1- Cleaning: we first fill the holed_ columns of the train data with the information present in y_train. We then remove columns that has missing values. We then devide the X_test into two data files. The first one contains a complete history of electricity consumption of 30000 users, the second one contains the test data (1000 users).

2- To predict the missing electricity consumption values of 1,000 users, I used a nearest-neighbor approach based on similarity in consumption patterns. Specifically, for each user with missing values, I identified the 7 most similar users from the complete dataset (50,000 users) using the Euclidean distance. These nearest neighbors were used to impute the missing values.

To handle the large scale of the data efficiently, the process was GPU-accelerated using a function fill_missing_with_closest_columns_gpu, which allowed for fast computation of pairwise distances and batch-wise processing (batch size = 100). This significantly reduced runtime while maintaining prediction accuracy.

3. Code: will be available soon.

4. Kmeans.ipynb and Elbow.. are not part of the solution but can be usefull to better understand the problem.

