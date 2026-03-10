# CNN vs RNN on MNIST – Performance Comparison using PyTorch
## Overview

This project compares the performance of a Convolutional Neural Network (CNN) and a Recurrent Neural Network (RNN) on the MNIST handwritten digit dataset.

The goal was to understand how architecture choice affects performance on image classification tasks.

## Dataset
- MNIST Handwritten Digits
- 60,000 training images
- 10,000 test images
- Image size: 28 * 28 (grayscale)

## Models Implemented
### 1. CNN Architecture
- Conv2D(1, 32, kernel = 3, padding = 1)
- MaxPooling(2 * 2)
- Conv2D(32, 64, kernel = 3, padding = 1)
- MaxPooling (2 *2)
- Fully Connected( 3136 -> 256)
- Output Layer(256 -> 10)
Accuracy: 99.15%

### 2. RNN Architecture
- RNN(hidden_dim = 150, layers = 1)
- Fully connected Layer
- Output Layer(-> 10)
Accuracy: 96.87%

## Results & Insights
- CNN significantly outperformed RNN
- CNN captures 2D spatial features effectively.
- RNN processes images sequentially, losing spatial locality.
- Confusion matrix analysis showd RNN Struggled with visually similar digits.

## Confusion Matrix

<img width="1086" height="990" alt="confusion matrix minst data" src="https://github.com/user-attachments/assets/d8bc4173-78b5-46a0-a816-4b9659fd4024" />

## Technologies Used
1. Python
2. Scikit-learn
3. PyTorch - Model building and training
4. Torchvision - MNIST dataset and image utilities
5. Torchvision Transforms - Data preprocessing
6. Torch Optim - Optimization algorithms
7. Matplotlib - Visualization
8. Seaborn - Confusion matrix heatmaps

