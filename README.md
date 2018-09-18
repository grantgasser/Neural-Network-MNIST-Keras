# Simple Neural Network

### Description
This notebook implements a very simple neural network for the MNIST dataset of handwritten images. The goal is to to have the
model correctly classify as many images as possible. One can see that using a library such as keras can lead to admirable results
(at least compared to the early days of neural nets) with a vanilla neural network. 

### Parameters and network features
Without using cross validation for parameters such as the regularization constant, # of layers, # of units in each layer, and many other 
considerations with neural nets, one can see that the network with 5 layers (3 hidden) works quite well (~90% test accuracy). 
The input dimension is 784 (28x28 px images). 
The activation function for each layer is the RELU = max(z, 0), where z = x'w and where x is the data (or the vector of outputs from the previous layer) and w is the vector of weights for that layer. The output layer is softmaxed to get a probability distribution for each example. The model predicts the value with the highest probability. We use the Adam optimizer. Results are much similar to stochastic gradient descent (SGD) in this case. The loss is measured as the categorical cross entropy of the output layer distribution.

#### Notes
See the [Keras Documentation](https://keras.io/) for specifics.

