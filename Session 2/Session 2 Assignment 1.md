# Session 2 Assignment 1 

# Visualization of steps for Neural Network

## by Abhishek Sakhapariya

### Step 0: Read input and output

#### Input

| X    |      |      |      |
| ---- | ---- | ---- | ---- |
| 0    | 1    | 0    | 1    |
| 1    | 0    | 1    | 0    |
| 1    | 0    | 1    | 1    |

#### Output

| Y    |
| ---- |
| 1    |
| 1    |
| 0    |



### Step 1: Initialize weights and biases with random values (There are methods to initialize weights and biases but for now initialize with random values)

| wh   |      |      |
| ---- | ---- | ---- |
| 0.25 | 0.33 | 0.37 |
| 0.09 | 0.59 | 0.62 |
| 0.27 | 0.54 | 0.39 |
| 0.88 | 0.55 | 0.1  |

| bh   |      |      |
| ---- | ---- | ---- |
| 0.6  | 0.42 | 0.17 |

| wout |
| ---- |
| 0.8  |
| 0.2  |
| 0.5  |

| wout |
| ---- |
| 0.8  |
| 0.2  |
| 0.5  |



### Step 2: Calculate hidden layer input:
#### hidden_layer_input= matrix_dot_product(X,wh) + bh

| hidden_layer_input |      |      |
| ------------------ | ---- | ---- |
| 1.57               | 1.56 | 0.89 |
| 1.12               | 1.29 | 0.93 |
| 2                  | 1.84 | 1.03 |



### Step 3: Perform non-linear transformation on hidden linear input

#### hiddenlayer_activations = sigmoid(hidden_layer_input)

| hidden_layer_activation |      |      |
| ----------------------- | ---- | ---- |
| 0.83                    | 0.83 | 0.71 |
| 0.75                    | 0.78 | 0.72 |
| 0.88                    | 0.86 | 0.74 |



