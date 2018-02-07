# neural-network-framework
This is a neural network framework that I designed myself becuase I was looking for something simple and easy to use in Java and I couldn't find anything that fit that description.

To create an instance of the NeuralNetwork class, simply type "new NeuralNetwork(int_array)" where int_array is the shape of the neural network. For instance, [3,4,2] as a value for int_array would create a neural network with three inputs, two outputs, and one hidden layer with four nodes.

Setting neural network properties is easy to do, though limited in scope. To set the acceptable error for a training sample, use the method setErrorThreshold. To set the constant learning rate of the network, use setLearningRate. To change the activation function, use setActivationFunction with the input "TANH" or "SIGMOID" for the respective activation function.

You can save and load neural networks using the methods save and load with the name of the text file. For example, NN.save("example.txt") will create a text file with the name "example.txt" with all the edge weights. NN.load("example.txt") will set the weights of NN to the saved weights in "example.txt." It does not save other properties of the network though. Those will need to be input every time.

To run the examples on the network to train, create an instance of class Example using input and output double arrays or just an input array. To train a network, the command is simply train and takes in a list of Examples and a number of times for it to loop over the data (this is only approximate because it pulls Examples at random, so on average it will run through each data point this many times).

To predict with the network, use the calculate method with an Example as input. This will return the predicted output for that Example.
