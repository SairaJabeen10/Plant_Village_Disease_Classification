# Plant Disease Classification Using Computer Vision

## Overview

This project focuses on plant disease classification using image processing and deep learning techniques. The PlantVillage dataset is used to identify different plant diseases from leaf images.

The project applies image preprocessing, feature enhancement, edge detection, and deep learning models to classify plant diseases accurately.

---

## Objectives

* Perform image preprocessing and enhancement.
* Apply Computer Vision techniques for feature extraction.
* Detect image edges using Sobel and Laplacian filters.
* Train a Fully Connected Neural Network (FCNN).
* Implement Transfer Learning using MobileNetV2.
* Compare model performance for plant disease classification.

---

## Dataset

**Dataset:** PlantVillage Dataset

The dataset contains thousands of leaf images belonging to different healthy and diseased plant classes.

---

## Image Preprocessing

The following preprocessing steps were applied:

* Image resizing (64×64)
* Grayscale conversion
* Histogram Equalization
* Image normalization

These steps improve image quality and help the model learn more meaningful features.

---

## Computer Vision Techniques

### Edge Detection

The following filters were applied:

1. Sobel X Filter
2. Sobel Y Filter
3. Laplacian Filter

These filters help highlight disease patterns and leaf structures.

---

## Deep Learning Models

### 1. Fully Connected Neural Network (FCNN)

Architecture:

* Flatten Layer
* Dense (128, ReLU)
* Dense (64, ReLU)
* Output Layer (Softmax)

### 2. Transfer Learning – MobileNetV2

Features:

* Pretrained on ImageNet
* Global Average Pooling
* Dense Layer
* Dropout Layer
* Softmax Output

Fine-tuning was performed on the final layers to improve classification performance.

---

## Technologies Used

* Python
* OpenCV
* NumPy
* Matplotlib
* TensorFlow
* Keras
* Scikit-Learn

---

## Workflow

Dataset Collection
→ Image Preprocessing
→ Histogram Equalization
→ Edge Detection
→ Data Normalization
→ Train-Test Split
→ FCNN Training
→ MobileNetV2 Transfer Learning
→ Fine-Tuning
→ Model Evaluation

---

## Results

* Image preprocessing improved feature visibility.
* Edge detection highlighted disease-affected regions.
* MobileNetV2 achieved better performance than the basic FCNN.
* Transfer learning improved classification accuracy and generalization.

---

## Author

**Saira Jabeen**
BS Artificial Intelligence
