# Machine Learning notes 


## Derivative, Gradient, Jacobian, Hessian

- Derivative represents the slope of the tangent of a function. It points in the direction of the greatest rate of increase of the function.
- Gradient is a multi-variable generalization of the derivative. The gradient is a vector-valued, while the derivative is a scalar-valued.
- Jacobian is a matrix that contains the first-order partial derivatives of all the variables of a function.
- Hessian is a matrix that contains the second-order partial derivatives of all the variables of a function.


## Sigmoid, Softmax
- Sigmoid is used for multi-label classification, whereas softmax is used for multi-class classification.
- Sotmax output is a probability vector that shows the probability of assigning the input of classifier to each of the output classes.
- Cross-entropy loss can  be applied to the softmax output in order to measure the difference between the predicted (i.e., classifiers' scores) probability and the true (i.e. one-hot-encoding of the label) probability. 
- Sigmoid output can be considered as a binary probability distribution which shows the probability of class 'y' and class 'not y' (i.e., 1-y).


## Batch size

- Batch Gradient Descent : each batch contains the whole dataset
  - can covnerge to the global minima of the cost function (for convex functions)
  - slow training speed
- Stochastic Gradient Descent : each batch consists of 1 sample.
- Mini-batch Gradient Descent : batch size is more than 1 and the less than the whole data
  - faster convergence to a local minima of the cost function

training advice:
start with a small batch size and gradually increase it


## Momentum

Moving in the direction of gradient guides us sharply towards the local optimum. If a function has a large number of curvatures with different local optima, then moving in the direction of gradient will lead to oscillation and many sudden changes in the direction of movement. Momentum smooths out the path of movement by keeping a small fraction of previous direction.
