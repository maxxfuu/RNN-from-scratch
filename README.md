# RNN-from-scratch 

 The idea behind using a RNN is that knowing your data has a sequential relationship. If you were trying to predict a weather, yesterdays weather, todays weather, and tomorrows weathers are all in relation to each other. Therefore you let the RNN learn the data given that the data has a sequential relationship. \
 
 Whats not efficient is just feeding a dense network some values and have it figure out the the sequential relationship. Such that position 1 is related to position 2, and position 2 is related to position 3. 

 ## High-Level Overview 
![Unrolled RNN](images/RNN_Overview.png)