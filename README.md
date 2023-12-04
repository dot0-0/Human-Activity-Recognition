# Human-Activity-Recognition

## Table of Contents
- [About](#about)
- [Dataset](#dataset)
- [Network Architecture](#network-architecture)
- [Results](#results)
- [Requirements](#requirements)

## About
Recent years have seen a rise in interest in HAR research due to the rapid advancement of wearable sensor technology and the widespread availability of smart devices, such as gyroscopes and accelerometers built into smartphones. The methodology we present in this study automatically extracts spatial and temporal elements from smart device sensory data for the purpose of classifying HAR data. The method used to accomplish this is a hybrid supervised learning architecture made up of an LSTM (Long Short Term Memory) and a CNN (Convolutional Neural Network).

## Dataset 

UCI HAR Dataset - [UCI HAR Dataset](https://archive.ics.uci.edu/dataset/240/human+activity+recognition+using+smartphones)

## Network Architecture

This network architecture consists of two sequential 1-D CNN layers followed by an LSTM layer, an Attention layer, a flattened layer, and a dense layer, as illustrated in Figures 2 and 3.

In the initial CNN layer, we use a kernel size of 6, a stride of 1, and 2 paddings along with a ReLU activation function. Then, we apply max-pooling with a kernel size of 2. The input and output channels are adjustable based on the dataset configurations. The second CNN layer employs 64 input channels, 128 output channels, a kernel size of 3, a stride of 1, and 2 paddings, followed by a ReLU activation function. Similar to the first layer, max-pooling with a kernel size of 2 is used, and to prevent overfitting, a dropout rate of 0.1 is applied.

To capture bidirectional information, an LSTM network with 128 hidden sizes and a tanh activation function is employed. An attention mechanism is integrated to selectively merge and emphasize crucial features by recalculating weights and scores. Finally, a fully connected layer is utilized for the classification task.

During training, the model is trained for 50 epochs using a learning rate of 0.0025 and a batch size of 64. The Adam optimizer is utilized for optimizing the model's learning rate.

## Results
#### Without Attention
Accuracy: 91.65%
F1 Scores: 0.92

#### With Attention
Accuracy: 89.07%
F1 Scores: 0.87

## Requirements

Python 3.9

Pytorch 

## References

[https://github.com/jindongwang/Deep-learning-activity-recognition.git](https://github.com/jindongwang/Deep-learning-activity-recognition.git)

