# NNclassifier

## The class has the following functionality:
  - The class represents a Neural Network Classifier
  - When initializing the class, you will provide a list “layers” of 2-tuples.
  - The ith 2-tuple represents the ith layer.
  - The first element in the 2-tuple would be the number of neurons in that layer (an int)
  -  The second element would be a string from the set of strings:
      + "relu
      + “softmax”
      + "linear"

  - Example for the layers list: [(5, “relu”), (3, “relu”), (4, “linear”), (7,
  “softmax”)]
  - The first layer should have the same neurons as the number of columns in X.
  - The last layer should have the same neurons as the number of classes in y.
  - For simplicity, assume that the loss function used internally will always
  be thecategorical cross entropy loss: categorical_cross_entropy_loss(y, yHat)
  - Apart from the constructor, there are two methods which should be
  implemented:
    + predict(X) : Should run the “forward propagation” step without keeping
    track of gradients. If your input is a matrix X with N rows, then the output
    should be having N rows and the number of columns == number of outpu
    neurons.
    + fit_once(X, y, alpha): y will be a vector of integers. X will be a
    matrix. alpha is the learning rate. fit_once should perform:

      * One round of forward propagation
      * One round of back propagation
      * One round of weight update through gradient descent
    + For fit_once(X, y) assume that whatever is in X and y will be
    collectively used to perform one step of weight update. In the sense that,
    the decision to perform stochastic gradient descent VS “regular” full-batch
    gradient descent VS minibatch gradient descent is not the role of
    fit_once(). Rather, if you wish to perform SGD, ensure that each call to
    fit_once() has exactly one row in X. And so on.
