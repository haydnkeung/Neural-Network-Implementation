# Neural network implementation (from scratch) for binary classification
This is a binary classifier that uses a convoluted neural network to classify whether a picture is a cat or a dog.

The binary classifier accepts a picture of a cat/dog as its input and returns either 0 (it's a cat) or 1 (it's a dog) as the output.

## Picture to vector
The classifier first converts a 64x64 px image into three matricies. Each matrix represents the intensity of the amount of red, green and blue for a specific pixel in an image.

Afterwards, the three matricies are stacked together to form an input feature vector denoted as "x".

![Cat To Vector](cat_to_vector.png)

## Network architecture

Initial iterations of this project utilized logistic regressions and tanh functions as the hidden layer. However, it was observed that for large inputs to the activation function, the gradient became very small making the learning rate very slow. For now, the RELU activation function is used for the hidden layers. For the output layer, a logistic regression is used since the range of the function in between 0 and 1 making it a suitable choice to represent the probability of a picture being a dog. 1 denotes with 100% probability that the picture is a dog and 0 denote 0% probability being a dog (hence the picture is a cat).
