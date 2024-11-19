# Melanoma Detection Project

This project focuses on classifying skin cancer images using Convolutional Neural Networks (CNNs). The dataset used is from the ISIC (International Skin Imaging Collaboration) archive. Data augmentation techniques, along with dropout, batch normalization, and L2 regularization, were applied to enhance model performance and minimize overfitting.

## Table of Contents
- [General Information](#general-information)
- [Technologies Used](#technologies-used)
- [Data Augmentation](#data-augmentation)
- [Model Architecture](#model-architecture)
- [Results](#results)
- [Acknowledgements](#acknowledgements)

## General Information

The goal of this project is to develop a CNN-based model that classifies skin lesions into various skin cancer categories. The dataset contains images of different types of skin lesions, and the aim is to build a model that can classify new, unseen data with high accuracy.

- **Objective**: Build a CNN classifier for skin lesion images.
- **Dataset**: Images sourced from the ISIC dataset.
- **Challenge**: The dataset is imbalanced, requiring the use of data augmentation techniques to generate synthetic samples and balance the classes.

## Technologies Used

- **TensorFlow**: v2.17.0
- **Augmentor**: v0.2.12
- **NumPy**: v1.26.4
- **Matplotlib**: v3.7.1
- **Pandas**: v2.1.4

## Data Augmentation

To address class imbalance and improve the model's ability to generalize, the following data augmentation techniques were applied:

- Random horizontal and vertical flips
- Random rotation (up to 20 degrees)
- Random zoom (up to 20%)
- Random contrast adjustment

## Model Architecture

The CNN model consists of several convolutional blocks with batch normalization and dropout layers to mitigate overfitting. The architecture includes:

- **Input**: 180x180x3 images (scaled between 0-1)
- **Convolutional Layers**: 4 layers with 32, 64, 128, and 256 filters
- **MaxPooling2D**: After each convolutional block
- **Dropout**: 30-50% to reduce overfitting
- **Dense Layer**: 256 units with dropout
- **Output Layer**: Softmax activation for multi-class classification

**Loss Function**: Sparse Categorical Crossentropy (for integer labels)  
**Optimizer**: Adam optimizer with a learning rate schedule

## Acknowledgements

This project was inspired by the ISIC Skin Cancer Classification challenge.

