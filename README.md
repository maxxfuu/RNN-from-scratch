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

<img src="images/rnn_operations.svg" alt="RNN Operations" width="600" height="400"/>

![RNN Operations](images/rnn_operations.svg)

Let's break down the image above. 
1. We begin by passing in a single temperature element such as 64. 
1. Multiply that by the input weight 
1. After the multiplication we are left with XI, (X multiplied by I)
1. Moving forward, we pass the product into the the hidden step where it sums up the value that was just passed in, along with the product of the previous hidden steps input and its respective weights. 
1. After that we apply a non linear activation function and it gives us XH for the given time step. 
1. It the feeds XH(t1) to the ouput layer and it gets multiplied by the output weights. 