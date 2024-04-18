# RNN-from-scratch 

 The idea behind using a RNN is that knowing your data has a sequential relationship. If you were trying to predict a weather, yesterdays weather, todays weather, and tomorrows weathers are all in relation to each other. Therefore you let the RNN learn the data given that the data has a sequential relationship. \
 
 Whats not efficient is just feeding a dense network some values and have it figure out the the sequential relationship. Such that position 1 is related to position 2, and position 2 is related to position 3. 

 ## High-Level Overview 
![Rolled and Unrolled RNN](images/RNN_Overview.png)

input, hidden(recurrent step/recurrence), output layer. 
Magic happens in hidden layer, as shown the arrow depicts the recurrent nature of this architechture. 

Hidden step is conneted to future hidden steps for sequencial elements. The hidden step passes the value in two directions such that it passes to the output layer and the next sequence element. Each hidden step has knowledgeo of previous hidden step values because it is being passed forward sequentially. 

At a really high level, the RNN can "feed each sequence elelnbt both to the output and forward to the next sequence element so that network builds a memeory of the sequence. 

## Feed Forward RNN 

![RNN Operations](images/rnn_operations.svg)