# ML EIP-2 B1 | Session 1 Assignment

## by Abhishek Sakhapariya (abhishek.sakhaparia@gmail.com)

[TOC]

### Primary Task 

For this Session's assignment, primary task is to write 50-100 words articles for 7 topics.

#### 1. Convolution

In mathematical terms, Convolution means deriving a function C from given function A and B. Meaning of this terms involves end result C as well as execution of computation on functions A and B.

In Machine Learning and Neural Networks terms, Convolution is a process of computation applied to input data of one layer and passing output to next layer.

For, example in session 1 we observed how an 3x3 Filter / Kernal explained in next topic is used for an image's Convolution in effort to observe different feature, which will be explained in later topic. 

#### 2. Filters / Kernels

In process of Convolution function A which is usually raw data or input of processed data from previous layer is processed with function B also referred as Filters or Kernels to derive output for results or Next layer's input in a network. 

Ideal Filter or Kernel size is 3x3 due to compute friendly nature, meaning GPUs primarily being utilized for purpose of such computation are more optimal in terms of taking less time for 3x3 kernels compared to other kernel options,  and may be consuming less energy (a hunch that may need to be looked on web). 

#### 3. Epochs

Epoch is a term used to indicate how many time whole data set has been passed by an algorithm. 

Only 1 Epoch is not enough to train a Neural Network and leads to underfitting and more the numbers of Epochs in Neural network better chance of getting acceptable accuracy. 

Hence, usually Neural Networks require thousands of Epoch to become trained and accurate in a given task.

#### 4. 1x1 Convolutions

At some point in Neural networks training there comes a point when there are too many channels and good chance many of them can be merged due to similarities. 

1x1 Convolutions comes in to picture at this point to with purpose to combine channels by focusing on 1 pixel of an image; while avoiding removing important channels as well as making sure to remove duplicates with help of back propagation. 

For eg. we have 120x120 data set with 1024 channels if we put it in to 3x3 convolution its going to take huge amount of time due to sheer size of channels and to reduce size of channels we will use 1x1x1024 with 64 to make things more manageable. 

![1x1_Convolution](https://cdn-images-1.medium.com/max/1600/1*so7PjTzE7SKeXf0mn38dyg.png)

#### 5. 3x3 Convolutions

A 3x3 Convolution happens with a 3x3 Filter / Kernal meaning a 3x3 area of input will be observed at a time.

Following gif taken form a blog post on hackernoon shows how a 3x3 convolution would happen. 

![3x3_Convolution](https://cdn-images-1.medium.com/max/800/1*ZCjPUFrB6eHPRi4eyP6aaA.gif)

#### 6. Feature Maps

As observed in session, a feature map is built using a Filter / Kernal on top of an image meaning Feature map is mapping of a feature on a image / input. 

A filter / kernal in this case can represent shape, color hue, etc and a feature map with that will show a active areas for the input where that feature was present.

#### 7. Feature Engineering

Feature Engineering is process of creating features for ML algorithms to work on. 

A feature can be any property or attribute that may be useful to build a ML model.

Process of feature engineering can be done manually or with automated.

A good example for automated feature engineering is with CNN where human intervention is low or negligible.



### Bonus points if you write on any of these:

#### * Activation Function

While every layer of a neural network process input X1,..Xn with a kernel A1,..,An and provides output Y1,..,Yn. 

An activation function at end of layers provides valuable insight on weather output by neuron can be considered as activated or not; creating a unique patter in the neural network.

For eg. for a kernel that identifies color blue in an image only the segments that are blue in the image will be activated for that kernel for that input image. 

#### * How to create an account on GitHub and upload a sample project



#### * Receptive Field

A Receptive field on human body simply means a sensory neuron that is place to sense one particular kind of input. 

In neural network terms a receptive field is nothing but a input space which effects output unit of a network.

#### * 10 examples of use of [MathJax (Links to an external site.)Links to an external site.](https://support.typora.io/Markdown-Reference/#math-blocks) in Markdown

1. Euler's identity: 

$$
\begin{equation*}
   e^{\pi i} + 1 = 0
\end{equation*}
$$

2. Friedmann Equations

$$
\begin{equation*}
   ( a^2 + k c^2 ) / a^2 = (8 \pi G p + A c^2 ) / 3 
\end{equation*}
$$

3. 

$$
for \space every \space X=Y^2, \delta X / \delta Y = 2Y
$$

4. The Gaussian Integral

$$
\int e^{x^2} \, dx = \sqrt{\pi}
$$

5. The Analytic Continuation of the Factorial

$$
n! = \int_0^\infty x^n e^{-x} \,dx
$$





### References:

1. https://medium.com/machine-learning-bites/deeplearning-series-convolutional-neural-networks-a9c2f2ee1524 - Image used in topic 4 was taken form this post
2. https://hackernoon.com/visualizing-parts-of-convolutional-neural-networks-using-keras-and-cats-5cc01b214e59 - Image used in topic 5 was taken from this post