# Neural-Network-Implementation-for-MNIST-Classification
This deep learning project involves designing and implementing a neural network from scratch using PyTorch for classifying handwritten digits from the MNIST dataset. 
The project emphasizes a deep understanding of forward and backward propagation, training neural networks, and improving performance with regularization techniques.

# Neural Network Implementation for MNIST Classification

This project involves designing and implementing a neural network from scratch using PyTorch for classifying handwritten digits from the MNIST dataset. The project emphasizes a deep understanding of forward and backward propagation, training neural networks, and improving performance with regularization techniques.

## Project Overview

The primary objective of this project was to classify images of handwritten digits (0–9) from the MNIST dataset using a fully connected neural network. Key learning outcomes include:
- Building and training neural networks from scratch.
- Experimenting with regularization techniques such as L2 regularization and Batch Normalization.
- Analyzing the impact of hyperparameters on model performance.

## Dataset

The MNIST dataset consists of grayscale images of handwritten digits, each of size 28×28 pixels. 

- **Train Set:** 80% of the data
- **Validation Set:** 20% of the training data
- **Test Set:** 20% of the total dataset

### Data Preprocessing
1. **Normalization**: Pixel values were scaled to the range [0, 1].
2. **One-Hot Encoding**: Labels were converted to one-hot format.
3. **Flattening**: Each image was reshaped into a 1D vector of size 784.

## Neural Network Architecture

The network has a four-layer architecture:
- **Input Layer:** 784 neurons (flattened image size)
- **Hidden Layers:**
  - Layer 1: 20 neurons, ReLU activation
  - Layer 2: 7 neurons, ReLU activation
  - Layer 3: 5 neurons, ReLU activation
- **Output Layer:** 10 neurons (one for each digit), SoftMax activation

### Training Configuration
- **Learning Rate:** 0.009
- **Batch Sizes:** {32, 64, 128}
- **Epochs:** Up to 100
- **L2 Regularization:** {0.01, 0.04}
- **Stopping Criteria:** Training stops if the validation cost does not improve for 100 consecutive iterations with a threshold of 0.00001.

## Key Features

1. **Batch Normalization**
   - Applied after activation to stabilize learning and speed up convergence.

2. **L2 Regularization**
   - Regularization strength (λ) set to 0.01, effectively reducing overfitting while maintaining model flexibility.

## Results and Insights

### Best Configuration
- **Batch Size:** 32
- **Epochs:** 100
- **L2 Regularization:** λ = 0.01

### Metrics
- **Train Accuracy:** 94.23%
- **Validation Accuracy:** 92.73%
- **Test Accuracy:** 92.93%

### Observations
1. Smaller batch sizes provided smoother and faster convergence.
2. L2 regularization significantly improved generalization performance.
3. Batch normalization was effective when combined with L2 regularization but could introduce numerical instability when used alone.

## Contributors

- **Adi Maman** - [Email](mailto:adimaman22@gmail.com)
- **Eran Fishbein** - [Email](mailto:"eranfish76@gmail.com" <eranfish76@gmail.com>)

For detailed information about the implementation, refer to the [project report](https://github.com/adimaman22/Neural-Network-Implementation-for-MNIST-Classification/blob/main/Neural%20Network%20Implementation%20for%20MNIST%20Classification%20-%20report.pdf).

