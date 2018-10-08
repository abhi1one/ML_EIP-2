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



### Step 4: Perform linear and non-linear transformation of hidden layer activation at output layer

#### output_layer_input = matrix_dot_product (hiddenlayer_activations * wout ) + bout 

#### output = sigmoid(output_layer_input) 

| output |
| ------ |
| 0.85   |
| 0.84   |
| 0.86   |



### Step 5: Calculate gradient of Error(E) at output layer

#### E = y-output

| E     |
| ----- |
| 0.15  |
| 0.16  |
| -0.86 |



### Step 6: Compute slope at output and hidden layer

#### Slope_output_layer= derivatives_sigmoid(output)

| Slope output |
| ------------ |
| 0.13         |
| 0.13         |
| 0.12         |

#### Slope_hidden_layer = derivatives_sigmoid(hiddenlayer_activations)

| Slope Hidden Layer |      |      |
| ------------------ | ---- | ---- |
| 0.14               | 0.14 | 0.21 |
| 0.19               | 0.17 | 0.20 |
| 0.10               | 0.12 | 0.19 |



### Step 7: Compute delta at output layer

#### d_output = E * slope_output_layer*lr

| Delta output |
| ------------ |
| 0.02         |
| 0.02         |
| -0.10        |



### Step 8: Calculate Error at hidden layer

#### Error_at_hidden_layer = matrix_dot_product(d_output, wout.Transpose)

| Error at Hidden Layer |        |        |
| --------------------- | ------ | ------ |
| 0.015                 | 0.004  | 0.009  |
| 0.016                 | 0.004  | 0.010  |
| -0.083                | -0.021 | -0.052 |



### Step 9: Compute delta at hidden layer

#### d_hiddenlayer = Error_at_hidden_layer * slope_hidden_layer

| Delta Hidden Layer |         |         |
| ------------------ | ------- | ------- |
| 0.0038             | 0.0039  | 0.0056  |
| 0.0042             | 0.0043  | 0.0062  |
| -0.0211            | -0.0215 | -0.0313 |

| Learning Rate |
| ------------- |
| 0.1           |

### Step 10: Update weight at both output and hidden layer 

#### wout = wout + matrix_dot_product(hiddenlayer_activations.Transpose,  d_output)*learning_rate

| wout from stpe10 |
| ---------------- |
| 0.294            |
| 0.244            |
| 0.225            |

#### *wh =  wh+ matrix_dot_product(X.Transpose,d_hiddenlayer)*learning_rate

| wh    |       |       |
| ----- | ----- | ----- |
| 0.248 | 0.328 | 0.367 |
| 0.090 | 0.590 | 0.621 |
| 0.268 | 0.538 | 0.387 |
| 0.878 | 0.548 | 0.097 |

### Step 11: Update biases at both output and hidden layer

#### bh = bh + sum(d_hiddenlayer, axis=0) * learning_rate

| bh    |       |       |
| ----- | ----- | ----- |
| 0.599 | 0.420 | 0.170 |

#### bout = bout + sum(d_output, axis=0)*learning_rate

| bout based on step 11 |
| --------------------- |
| 0.564                 |

