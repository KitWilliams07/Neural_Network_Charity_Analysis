# Neural_Network_Charity_Analysis

## Overview of the Analysis

The point of this analysis was to use a neural network to create a binary classifier to predict if applications will be successful if funded by Alphabet Soup. That dataset contains more than 34,000 organizations that have recieved funding from Alphabet Soup with various columns highlighting specific features of the fund, in addition to whether it was successful or not. These features will be used to train the neural network and be used to predict the potential success of future funds. 

## Results

Data Preprocessing:

What variable(s) are considered the target(s) for your model?
- The target variable for the model was whether or not the fund was successful or not. There was a column in the dataset labeled 'Is Successful' with a 0 indicating 'No' and a 1 indicating 'Yes'.

What variable(s) are considered to be the features for your model?
- Every other column in the dataset other than the target variable was considered a feature. Only after analyzing the variation of each column did we determine if it would be work as a feature. If the column had a large variance with many outliers it was not used as a feature due to concern it would lead to poor predictions.

What variable(s) are neither targets nor features, and should be removed from the input data?
- The only variable that I removed from the dataset was the "Ask Amount" Variable. Below is the count of each unique Ask Amount. Since there were 8,747 unique Ask Amounts, with the 2nd highest frequency being 3, it would have been difficult to bin this data. It essentially would have led to "Is the Ask Amount $5,0000 or something different?" which doesn't tell you much.  

![alt text](https://raw.githubusercontent.com/KitWilliams07/Neural_Network_Charity_Analysis/main/Challenge/Resources/ask_amt_counts.png)




## Summary 

The original Neural Network that was created had the following specifications:

Inputs: 43
Hidden Layer 1: 80 Neurons, Activation Funtion: Relu 
Hidden Layer 2: 30 Neurons, Activation Function: Relu
Output Layer: 1 Neuron, Activation Function: Sigmoid
Epochs: 30

Loss: 0.5555
Accuracy: 0.7312


The accuracy was 73%. The goal was now to optimize the network to improve the accuracy to over 75%. 

So a few steps were taken to try and increase model performance. First, an additional hidden layer was added in order to increase the computational complexity of the network. Also, more neurons were added to each network. The activation functions were kept the same: the hidden layers used the Relu (Recitifer) Function and the output layer used a Sigmoid Function. I didn't wish to change these functions because I like the Rectifier function on the hidden layers by eliminating a negative output to 0 and scaling the positive. This leads into the output layer which takes the sigmoid function and based on the positive values from the previous layers, it will convert to either a 0 or 1 which is what you want for a Binary Classifier. As discussed in the results section, I removed the Ask Amount column from the features. This now left my model with 39 inputs. Finally, the number of epochs was increased from 30 to 200. This was determined using trial and error without overfitting the model. So, below is the specifications to my neural network.


Inputs: 43
Hidden Layer 1: 100 Neurons, Activation Funtion: Relu 
Hidden Layer 2: 50 Neurons, Activation Function: Relu
Hidden Layer 3: 10 Neurons, Activation Function: Relu
Output Layer: 1 Neuron, Activation Function: Sigmoid
Epochs: 200

Loss: 0.5584
Accuracy: 0.7312


Oddly, the Loss and the Accuracy did not change. We did not reach the target model performance even after making several adjustments used to optimize results. Without creating an additional model and tweaking the specifications even further, it is hard to say why the network preformed the way it did.





