# Performance Analysis of Convolutional Neural Networks on CIFAR-10

> "The purpose of computing is insight, not numbers." — Richard Hamming

## Overview
This repository presents an in-depth study of Convolutional Neural Networks (CNNs) on the CIFAR-10 dataset, comparing various architectures, including:

- **Custom CNN Model** (incrementally improved with dropout, batch normalization, and data augmentation)
- **MobileNetV2** (fine-tuned with ImageNet weights)
- **AlexNet** (trained from scratch)
- **ResNet152V2** (evaluated with both ImageNet-pretrained and randomly initialized weights)

The study focuses on analyzing the impact of different training strategies, hyperparameters, and model complexities on classification performance.

## Key Achievements
- **ResNet152V2 with ImageNet weights achieved the highest test accuracy of 92.31\%**
- **Fine-tuning MobileNetV2 resulted in suboptimal performance (70.53\%)**, indicating that its lightweight architecture is not well-suited for CIFAR-10
- **AlexNet (60.11\%) struggled with small input sizes (32x32)** but served as a benchmark for evaluating CNN improvements
- **Custom CNN (90.5\%) demonstrated the effectiveness of incremental enhancements**, showcasing how dropout, batch normalization, and data augmentation improve generalization

## Methodology
- **Data Preprocessing:** Standardized and normalized CIFAR-10 dataset
- **Hyperparameter Tuning:** Explored optimizers, learning rates, and regularization techniques
- **Training Strategy:** Applied fine-tuning, dynamic learning rate scheduling, and model checkpointing
- **Evaluation Metrics:** Accuracy, loss, and confusion matrices

## Results
| Model                        | Test Accuracy | Loss  |
|------------------------------|--------------|-------|
| Custom CNN (Final)           | 90.5\%       | 0.3646|
| MobileNetV2 (Fine-tuned)     | 70.53\%      | 0.8097|
| AlexNet (From Scratch)       | 60.11\%      | 1.3035|
| ResNet152V2 (From Scratch)   | 62.35\%      | 1.0441|
| ResNet152V2 (Pretrained)     | 92.31\%      | 0.1159|

## Impact
- **Highlights the effectiveness of pretrained models for small datasets**
- **Demonstrates the necessity of depth and complexity for performance gains**
- **Validates the concept of "Neural Redshift"**, showing that models with <5M parameters struggle to generalize effectively
- **Provides insights into optimizing CNNs through hyperparameter tuning and training strategies**


## Conclusion
Pretrained models like ResNet152V2 significantly outperform training from scratch, highlighting the importance of transfer learning. The study also emphasizes the impact of architecture selection, hyperparameter tuning, and incremental enhancements in improving CNN performance on CIFAR-10.

