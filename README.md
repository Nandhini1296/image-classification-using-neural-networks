# image-classification-using-neural-networks

Implementation of a neural network to classify images of Dogs, Cats and Penguins

## Data

The training and testing data consists of the following:
 
 - The train/ folder consists of 1000 kitten images under cats/ and 1000 dog images under dogs/ and 1000 penguin images under penguins/.
 - The validation/ folder contains 400 images each, of more cats, dogs and penguins - these are to feed the trained network, compare its classification answers to the actual answers so we can compute the accuracy of the training.
 - The live/ folder contains new test images for the neural network to classify and output the class as 0 - for cats, 1 - for dogs, 2 - for penguins.
 
## Programs

In ```train.ipynb```, the network is set up and the training is done done using it. The results - learned weights, biases for each neuron in each layer are stored as ```weights.h5``` file. A .h5 file is a binary file format - hierarchial , JSON-like, perfect for storing network weights. 

The code uses the Keras NN library, which runs on graph (dataflow) execution backends such TensorFlow. The backprop loop runs 50 epochs through all the training data. The weights.h5 file can be viwed using HDFView-2.14.0 from [this link](https://support.hdfgroup.org/products/java/release/download.html).

The ```3class_classify.ipynb``` is used to classify and contains Keras code to read the weights file and associate the weights with a new model.

