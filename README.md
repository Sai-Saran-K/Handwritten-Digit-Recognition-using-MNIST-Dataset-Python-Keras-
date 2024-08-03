# Project Overview
This project involves solving a multi-class classification problem using the MNIST dataset, which contains images of handwritten digits (0-9). The goal is to build and compare two deep learning models: a Multi-Layer Perceptron (MLP) and a Convolutional Neural Network (CNN).

## Key Details
- **Language**: Python
- **Deep Learning Package**: Keras
- **Dataset**: MNIST dataset available with Keras

## Dataset Description
- **Training Set**: 60,000 images of 28x28 pixels each, with corresponding labels.
- **Test Set**: 10,000 images of 28x28 pixels each, with corresponding labels.

## MLP Model
### Model Definition:
- **Input Shape**: 784 (28x28 image flattened)
- **1st Hidden Layer**: 512 neurons, ReLU activation
- **Output Layer**: 10 neurons (one for each digit), Softmax activation

### Training Process:
- **Preprocessing**: Flatten images, convert to float, and scale to [0,1].
- **Optimizer**: Standard optimizer functions.
- **Loss Function**: Cross-entropy loss.
- **Metrics**: Accuracy.
- **Training**: Batch size of 60, 5 epochs.

### Results:
- **Training Accuracy**: ~99.4%
- **Test Accuracy**: ~99.3%

## CNN Model
### Model Definition:
- **Input Shape**: 28x28x1 (image as a 2D matrix)
- **Convolutional Layers**:
  - 32 filters of 3x3, ReLU activation
  - Maxpooling of 2x2
  - 64 filters of 3x3, ReLU activation
  - Maxpooling of 2x2
  - 64 filters of 3x3, ReLU activation
- **Flatten Layer**: Convert to column vector for Fully Connected Network (FCN)
- **FCN Layers**:
  - 64 neurons, ReLU activation
  - 10 neurons (one for each digit), Softmax activation

### Training Process:
- **Preprocessing**: Convert labels to one-hot encoding.
- **Optimizer**: Standard optimizer functions.
- **Loss Function**: Cross-entropy loss.
- **Metrics**: Accuracy.
- **Training**: Similar process as MLP with adjusted epochs and batch size.

### Results:
- **Training Accuracy**: ~99.4%
- **Test Accuracy**: ~99.3%

## Conclusion
The CNN model outperforms the MLP model by leveraging spatial information in the images, resulting in higher accuracy with fewer parameters.

## Key Metrics
- **MLP**:
  - **Number of Parameters**: 407,050
  - **Training Accuracy**: ~98.9%
  - **Test Accuracy**: ~98.0%

- **CNN**:
  - **Number of Parameters**: 93,322
  - **Training Accuracy**: ~99.4%
  - **Test Accuracy**: ~99.3%
