# LeNet on MNIST with TensorFlow/Keras

This project implements the classic LeNet architecture for handwritten digit recognition on the MNIST dataset, using TensorFlow and Keras. The model closely follows the original LeNet paper, using `tanh` activations and average pooling layers.
`ReLU` activation was also used to compare results.
---

## Table of Contents

- [Overview](#overview)
- [LeNet Architecture](#lenet-architecture)
- [Setup & Installation](#setup--installation)
- [Usage](#usage)
- [Results](#results)
- [References](#references)
- [License](#license)

---

## Overview

LeNet is one of the earliest convolutional neural networks, designed for handwritten digit recognition. This implementation uses the MNIST dataset, which consists of 70,000 grayscale images of digits (0-9).

- **Dataset:** [MNIST](http://yann.lecun.com/exdb/mnist/)
- **Framework:** TensorFlow / Keras

---

## LeNet Architecture

Input: 28x28 grayscale image

Conv2D: 6 filters, 5x5 kernel, activation='tanh'

AveragePooling2D: 2x2 pool size

Conv2D: 16 filters, 5x5 kernel, activation='tanh'

AveragePooling2D: 2x2 pool size

Flatten

Dense: 256 units, activation='tanh'

Dense: 84 units, activation='tanh'

Dense: 10 units (output), activation='softmax'

**Total parameters:** ~90,802

---

## Results

### Model with `ReLU` performed slightly better than original `tanh` activation.

Activation | epochs | train_accuracy | test_accuracy
--- | --- | --- | --- 
`tanh` | 22 | 0.9995 | 0.9806
`ReLU` | 20 | 0.9978 | 0.9815

> *Note: Actual results may vary depending on hardware and random initialization.*

---

## References

- [LeNet-5, Yann LeCun et al.](http://yann.lecun.com/exdb/lenet/)
