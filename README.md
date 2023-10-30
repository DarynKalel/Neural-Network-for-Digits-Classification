# Neural-Network-for-Digits-Classification

In this first project, I developed a simple feedforward neural network using Python and NumPy (the standard numeric library for Python). I started by implementing just a simple neuron, or perceptron, then defined the training algorithm for this simple model. The second part consists in defining a simple neural network to perform digits classification.

# Training Data

The dataset is made of four input vectors  x∈R3  and the corresponding desired target values  y . In the table below, each row is a single sample; the first three columns are the input vector components, whereas the last column is the target output.

  Input xi 		Output  y 
1	   1	   0	   1
1	   0	   0	   1
0	   1	   0	   0
0	   0	   0	   0

# Activation Function

There are several activation funcations: ReLU, Sigmoid, Tanh.
In this particular project I used the sigmoid function.

# Weight Initialization

I initialized them randomly, so that their mean is zero. The weights matrix maps the input space into the output space, therefore in this case  W∈R3×1

# Forward propagation

This means taking an input sample and moving it forward through the network, calculating the output of the network eventually.

For our single neuron this is simply  y^=σ(WTx) , where  x  is one input vector.

Each input sample is arranged as a row of the matrix X, therefore I can access the first row by X[0]. I store it in the variable X0 for easier access. 

# Backpropagation

The following step is updating the weights by propagating the error backwards in the network. How this is done depends on the activation function, and namely on its derivative.

# Two-layer Neural Network

I tried to develop more advanced NN than a single perceptron. 

Consider the following training set:

  Input		      Output
x1 	 x2 	 x3 	 y 
0	   0	   0	   1
0	   0	   1	   1
0	   1	   0	   1
0	   1	   1	   0
1	   0	   0	   1
1	   0 	   1	   0
1	   1	   0	   1
1	   1	   1	   1

Repeat all the steps above.

# Handwritten digits classification

I tried to apply a model in a real-world scenario. In particular, on a simple digits classification problem. The model turns out to be similar to the perceptron implemented in the beginning, but here I used softmax activation function and cross-entropy loss function. The idea is to create a model that has in input an image of a handwritten digit and that return a vector of 10 probabilities (one for each possible digit  0−9 ).

# Dataset
The dataset used is included in scikit-learn, one of the major Machine Learning libraries. The dataset is called load_digits and contains several hundreds of samples. Each datapoint is made of the handwritten digit image (or rather its 8×8 pixel representation), that are responsible the input of the given model, and the target digit value.

I used a hot-encoding and softmax activation fucntion for this task. They very useful when we have to deal with multiclassification tasks and when we have to turn numbers into  m  probabilities that sum to one. 

# Loss function - Cross Entropy
# Defined a training procedure.
