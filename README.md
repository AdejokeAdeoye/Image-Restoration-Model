# Image Restoration Model - Deep Learning

This project involves training a convolutional neural network (CNN) to restore images that have been intentionally corrupted by adding blocks. The CIFAR-10 dataset is used for training and evaluation.

## Table of Contents
- [Introduction](#introduction)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Implementation](#implementation)
- [Results](#results)
- [Conclusion](#conclusion)

## Introduction
The goal of this project is to develop a neural network model that can restore corrupted images. This involves corrupting images by adding blocks to them and then training a model to reconstruct the original images from the corrupted ones.

## Dataset
The CIFAR-10 dataset is used in this project. It consists of 60,000 RGB images across 10 classes, with each image being 32x32 pixels. The dataset is divided into 50,000 training images and 10,000 test images. The 10 classes are: airplane, automobile, bird, cat, deer, dog, frog, horse, ship, and truck.

## Methodology
1. **Data Corruption**: Images are corrupted by adding random rectangular blocks.
2. **Model Architecture**: A convolutional neural network (CNN) is designed to restore the corrupted images.
3. **Training**: The model is trained on the corrupted images.
4. **Evaluation**: The performance of the model is evaluated using quantitative and qualitative metrics.

## Implementation
### Data Corruption
The `corrupt_data` function randomly adds blocks of a specified size to the images to simulate corruption.

### Model Architecture
The `model_restore` function defines a CNN for image restoration.

### Training and Evaluation
For each level of corruption (10, 50, 100 blocks), the images are corrupted, the model is trained, and the results are evaluated.

### Visualization
Side-by-side comparisons of original, corrupted, and restored images are displayed.

## Results
### Quantitative Evaluation
The quantitative evaluation measures the numerical performance of the model using two metrics:

- **Loss**: The loss function calculates the difference between the predicted and actual images.
- **Structural Similarity Index (SSIM)**: SSIM measures the similarity between the predicted and actual images. A higher SSIM score indicates greater similarity.

The loss and Structural Similarity Index (SSIM) are used to evaluate the model's performance.

- **10 Blocks**:
  - Loss: 0.00014849301078356802
  - Average SSIM Score: 0.9951236423907652

- **50 Blocks**:
  - Loss: 0.0008357324404641986
  - Average SSIM Score: 0.9766488547403522

- **100 Blocks**:
  - Loss: 0.0026070885360240936
  - Average SSIM Score: 0.9529005617909444

### Qualitative Evaluation
The qualitative evaluation assesses the visual quality of the restored images. Visualizations show side-by-side comparisons of original, corrupted, and restored images. This evaluation helps assess how effectively the model is able to restore the corrupted parts of the images, with restored images closely resembling the original uncorrupted images.

## Conclusion
The model demonstrates a practical application of neural networks in image restoration. It shows that while the model performs well with fewer corrupted blocks, the restoration quality decreases as the number of corrupted blocks increases.
