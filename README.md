#  Plant Disease Classification Using Computer Vision

An image-based plant disease classification system developed using Computer Vision and Deep Learning techniques. The project uses the PlantVillage dataset to classify healthy and diseased plant leaf images and compares a custom CNN with MobileNetV2 transfer learning and fine-tuning.

---

##  Overview:

Plant diseases can significantly affect agricultural productivity and crop quality. Early identification of plant diseases can help in taking preventive measures and reducing potential losses.

This project develops an automated plant disease classification system using Computer Vision and Deep Learning techniques.

The project explores image preprocessing, computer vision-based feature extraction, convolutional neural networks, transfer learning, and fine-tuning for plant disease classification.

Three deep learning approaches were evaluated:

- CNN from Scratch
- MobileNetV2 with Frozen Base
- MobileNetV2 with Fine-Tuning

The best-performing approach was MobileNetV2 with Fine-Tuning.

---

## Objectives:

The main objectives of this project are:

- To develop an automated plant disease classification system.
- To classify healthy and diseased plant leaf images.
- To apply image preprocessing techniques to improve model training.
- To explore Computer Vision techniques for extracting useful visual information.
- To develop a CNN-based classification model.
- To use MobileNetV2 transfer learning for improved feature extraction.
- To fine-tune MobileNetV2 for plant disease classification.
- To compare the performance of different deep learning approaches.
- To evaluate the final model on unseen images.

---

## Dataset:

The project uses the **PlantVillage dataset**.

The dataset contains plant leaf images belonging to multiple plant species and healthy/diseased categories.

### Dataset Characteristics

- RGB plant leaf images
- Multiple plant species
- Multiple disease categories
- Healthy and diseased classes
- Images organized according to class

The dataset was downloaded from Kaggle and organized into class-wise folders.

### Dataset Split

The dataset was divided into:

| Split | Percentage |
|---|---:|
| Training | 80% |
| Testing / Validation | 20% |

This split allows the models to be evaluated on images that were not used during training.

---

## Image Preprocessing:

Image preprocessing was performed before training the models.

The preprocessing pipeline included:

- Image resizing
- Pixel normalization
- Image loading and preparation
- Computer Vision-based feature visualization

The images used by the deep learning pipeline were resized to:

**128 × 128 pixels**

Pixel values were normalized to the range:

**0–1**

These steps help provide consistent input to the neural network and improve training stability.

---

## 🔬 Computer Vision Feature Extraction

Computer Vision techniques were also explored to visualize important structures and patterns in plant leaves.

### Sobel Filter

The Sobel operator was applied in the X and Y directions to highlight horizontal and vertical edges.

### Laplacian Filter

The Laplacian operator was used to detect edges in different directions and emphasize texture and boundary information.

These techniques were used to investigate visual characteristics of plant leaves and disease-related patterns.

---

##  Deep Learning Models:

Three approaches were explored in this project.

### 1. CNN from Scratch

A custom Convolutional Neural Network was developed for plant disease classification.

The architecture includes convolutional layers, batch normalization, pooling, dropout, flattening, and dense classification layers.

The CNN learns disease-related visual features directly from the training images.

---

### 2. MobileNetV2 — Frozen Base

A pretrained **MobileNetV2** model was used as a feature extractor.

The pretrained base model was kept frozen while additional classification layers were added for the plant disease classification task.

The classification architecture includes:

- MobileNetV2 Base Model
- Global Average Pooling
- Dense Layer
- Batch Normalization
- Dropout
- Softmax Classification Layer

Transfer learning allows the model to use features learned from a large-scale pretrained model instead of learning all visual features from scratch.

---

### 3. MobileNetV2 — Fine-Tuning

The MobileNetV2 model was further fine-tuned for the plant disease classification task.

The final layers of the pretrained network were unfrozen and retrained so that the model could learn more domain-specific plant disease features.

Fine-tuning was used to improve feature representation and classification performance.

---

##  Model Performance:

The evaluated models produced the following validation accuracies:

| Model | Validation Accuracy |
|---|---:|
| CNN from Scratch | 82.84% |
| MobileNetV2 Frozen | 88.28% |
| **MobileNetV2 Fine-Tuned** | **92.06%** |

###  Best Performing Model:

**MobileNetV2 Fine-Tuned**

**Validation Accuracy: 92.06%**

The results indicate that MobileNetV2 transfer learning performed better than the custom CNN, while fine-tuning further improved the classification performance.

---

##  Model Comparison:

The comparison demonstrates the benefit of transfer learning for this classification task.

### CNN from Scratch

The custom CNN successfully learned disease-related patterns but achieved lower validation accuracy compared with MobileNetV2.

### MobileNetV2 Frozen

Using a pretrained MobileNetV2 feature extractor improved the classification performance compared with the CNN trained from scratch.

### MobileNetV2 Fine-Tuned

Fine-tuning allowed the pretrained network to adapt its learned features to plant disease images and achieved the highest validation accuracy of **92.06%**.

---

##  Model Evaluation:

The project evaluated model performance using classification accuracy.

The evaluation process also includes analysis such as:

- Confusion Matrix
- Classification Results
- Per-Class Performance
- Prediction Results

The final model can also be used to perform inference on leaf images and generate a predicted disease class.

---

##  Technologies Used:

### Programming Language

- Python

### Computer Vision

- OpenCV

### Deep Learning

- TensorFlow
- Keras

### Data Processing

- NumPy
- Pandas

### Visualization

- Matplotlib

### Machine Learning

- Scikit-Learn

### Models

- Custom CNN
- MobileNetV2
- MobileNetV2 Transfer Learning
- MobileNetV2 Fine-Tuning

---

##  Project Workflow:

```text
PlantVillage Dataset
        │
        ▼
Dataset Organization
        │
        ▼
Image Preprocessing
        │
        ├── Image Resizing
        ├── Normalization
        └── Feature Visualization
        │
        ▼
Computer Vision Processing
        │
        ├── Sobel Filtering
        └── Laplacian Filtering
        │
        ▼
Train / Test Split
        │
        ▼
Deep Learning Models
        │
        ├── CNN from Scratch
        │
        ├── MobileNetV2 Frozen
        │
        └── MobileNetV2 Fine-Tuned
        │
        ▼
Model Evaluation
        │
        ├── Accuracy
        ├── Confusion Matrix
        └── Classification Results
Repository Contents
Plant_Village_Disease_Classification/
│
├── OEL_CV_1 (1).ipynb
│
├── Plant Disease Classification (Report).pdf
│
└── README.md
```
## Notebook:

OEL_CV_1 (1).ipynb

Contains the implementation of:

Dataset preparation
Image preprocessing
Computer Vision techniques
CNN model
MobileNetV2 transfer learning
Fine-tuning
Model evaluation
Prediction

## Report:

Plant Disease Classification (Report).pdf

Contains the project documentation, methodology, models, challenges, solutions, and conclusion.

## How to Run:
1. Clone the Repository
git clone https://github.com/SairaJabeen10/Plant_Village_Disease_Classification.git
2. Open the Notebook

Open:

OEL_CV_1 (1).ipynb

using Jupyter Notebook, JupyterLab, or Google Colab.

3. Prepare the Dataset

Download the PlantVillage dataset and organize the images according to the class structure used in the notebook.

4. Run the Notebook

Execute the notebook cells in sequence to:

Load the dataset
Preprocess images
Prepare training and testing data
Train the CNN model
Train MobileNetV2
Fine-tune MobileNetV2
Evaluate model performance
Perform predictions

 ## Key Findings:

The project demonstrated the following:

Computer Vision techniques can help visualize important plant leaf structures.
A custom CNN can learn useful disease-related visual patterns.
Transfer learning with MobileNetV2 improves classification performance.
Fine-tuning allows the pretrained model to adapt to the plant disease domain.
MobileNetV2 Fine-Tuning achieved the highest validation accuracy of 92.06%.

 ## Challenges and Solutions:

| Challenge | Approach |
|---|---|
| Large image dataset | Image resizing |
| Uneven lighting conditions | Histogram Equalization |
| High-dimensional image data | CNN-based feature extraction |
| Limited training efficiency | Transfer Learning |
| Risk of overfitting | Dropout and Fine-Tuning |

 ## Future Improvements:

Possible future improvements include:

Testing the model on real-world field images.
Adding images captured under different lighting conditions.
Improving classification of visually similar diseases.
Adding more plant species and disease categories.
Deploying the trained model as a web application.
Developing a mobile application for plant disease detection.
Optimizing the model for mobile and edge devices.
Collecting a larger real-world dataset for improved generalization.

 ## Project Documentation:

The detailed project methodology and implementation are available in the project report:

Plant Disease Classification Using Computer Vision

The report covers the dataset, preprocessing, Computer Vision techniques, deep learning models, transfer learning, fine-tuning, evaluation, challenges, and conclusion.

## Author:
Saira Jabeen
Kainat Moin
Hafsa Naz
Sabiha Pirzadah

Artificial Intelligence Student

GitHub:
https://github.com/SairaJabeen10

## Acknowledgement:

This project was developed as an academic Computer Vision and Machine Learning project using the PlantVillage dataset and deep learning techniques.
        │
        ▼
Plant Disease Prediction
