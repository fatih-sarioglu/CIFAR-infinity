# CIFAR-infinity

## Overview

This repository contains implementations and performance comparisons of multiple deep learning architectures for image classification on the CIFAR-10 dataset. The project explores various state-of-the-art convolutional neural networks to evaluate their effectiveness in terms of accuracy, model size, and efficiency.

## Models Implemented

The following architectures have been implemented and evaluated:

- AlexNet
- VGG (with BatchNorm)
- Inception Network (with BatchNorm)
- ResNet
- MobileNet (standard and larger variant)
- EfficientNet

## Results Summary

### Performance Comparison

| Model | Test Accuracy (%) | Parameters (M) | Best Epoch | Training Accuracy (%) | Training-Test Gap (%) |
|-------|-------------------|----------------|------------|------------------------|------------------------|
| ResNet | 93.19 | 21.2 | 53 | 99.93 | 6.74 |
| EfficientNet | 92.65 | 17.4 | 69 | 99.45 | 6.8 |
| MobileNet | 90.75 | 1.0 | 65 | 99.94 | 9.19 |
| MobileNetBig | 90.10 | 3.2 | 58 | 99.87 | 9.77 |
| Inception + BatchNorm | 89.87 | 1.6 | 50 | 99.31 | 9.44 |
| VGG + BatchNorm | 86.58 | 33.6 | 50 | 95.29 | 8.71 |
| AlexNet | 77.53 | 3.2 | 50 | 81.97 | 4.44 |

### Key Findings

- **ResNet** achieved the highest test accuracy at 93.19% with 21.2M parameters
- **EfficientNet** delivered strong performance (92.65% accuracy) but with a larger implementation (17.4M parameters) compared to the paper's reported 4M parameter model achieving 98% accuracy
- **MobileNet** offers the best efficiency-to-performance ratio with 90.75% accuracy using only 1M parameters
- **AlexNet** shows the lowest overfitting (4.44% gap) but also the lowest overall accuracy

## Training Configuration

All models were initially configured for 150 epochs with early stopping implemented. Training was conducted on the CIFAR-10 dataset, which consists of 60,000 32x32 color images across 10 classes (50,000 training, 10,000 testing).

## Future Work

Potential areas for improvement:
- Optimizing the EfficientNet implementation to achieve better parameter efficiency
- Exploring more advanced data augmentation techniques
- Implementing ensemble methods to further boost accuracy
- Evaluating inference time and memory requirements for deployment considerations

### License and Usage

The code in these notebooks is available for anyone to use for any purpose without restrictions. You are welcome to use, modify, distribute, or build upon this work for academic, personal, or commercial applications. No attribution is required, though it is always appreciated. Feel free to adapt these implementations for your own projects or educational purposes.