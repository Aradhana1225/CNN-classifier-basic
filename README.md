# CNN Image Classifier -- CIFAR-10

A basic **Convolutional Neural Network (CNN)** image classification
project implemented using **TensorFlow/Keras**. The model is trained on
the CIFAR-10 dataset to classify images into 10 different categories.

> **Note:** This notebook is based on the TensorFlow CNN tutorial. The
> repository is intended as a learning/practice implementation of the
> concepts demonstrated in the notebook.

## 📌 Project Overview

The project demonstrates the complete workflow of building and training
a simple CNN:

1.  Load the CIFAR-10 dataset
2.  Normalize image pixel values
3.  Visualize sample images
4.  Build a CNN using convolution and max-pooling layers
5.  Add fully connected (Dense) layers
6.  Compile and train the model
7.  Evaluate the model on the test dataset
8.  Visualize training and validation accuracy

## 📊 Dataset

The **CIFAR-10** dataset contains:

-   60,000 color images
-   50,000 training images
-   10,000 test images
-   Image size: **32 × 32 × 3**
-   10 classes

### Classes

-   ✈️ Airplane
-   🚗 Automobile
-   🐦 Bird
-   🐱 Cat
-   🦌 Deer
-   🐕 Dog
-   🐸 Frog
-   🐎 Horse
-   🚢 Ship
-   🚚 Truck

## 🧠 CNN Architecture

The model uses the following architecture:

``` text
Input: 32 × 32 × 3
        ↓
Conv2D — 32 filters, 3×3, ReLU
        ↓
MaxPooling2D — 2×2
        ↓
Conv2D — 64 filters, 3×3, ReLU
        ↓
MaxPooling2D — 2×2
        ↓
Conv2D — 64 filters, 3×3, ReLU
        ↓
Flatten
        ↓
Dense — 64 neurons, ReLU
        ↓
Dense — 10 outputs
```

## ⚙️ Training Configuration

-   **Optimizer:** Adam
-   **Loss:** Sparse Categorical Crossentropy with logits
-   **Metric:** Accuracy
-   **Epochs:** 10
-   **Input:** CIFAR-10 RGB images
-   **Pixel normalization:** Pixel values divided by 255

## 📈 Result

The trained CNN achieved approximately:

**Test Accuracy: 70.87%**

The notebook also plots training accuracy and the accuracy obtained
using the test dataset during training.

## 🛠️ Technologies Used

-   Python
-   TensorFlow
-   Keras
-   NumPy
-   Matplotlib
-   Google Colab
-   Jupyter Notebook

## 📁 Repository Structure

``` text
CNN-classifier-basic/
│
├── cnn.ipynb
└── README.md
```

## ▶️ How to Run

### Option 1 --- Google Colab

Open `cnn.ipynb` in Google Colab and run the cells from top to bottom.

### Option 2 --- Local Environment

Install the required libraries:

``` bash
pip install tensorflow matplotlib numpy
```

Then open the notebook using Jupyter Notebook or JupyterLab.

## 🔍 What I Learned

This project provides hands-on practice with:

-   Image preprocessing
-   CNN fundamentals
-   Convolutional layers
-   Max pooling
-   Feature extraction
-   Flattening and Dense layers
-   Model compilation and training
-   Model evaluation
-   Accuracy visualization

## 🚀 Possible Improvements

Future versions could improve the baseline model by adding:

-   Data augmentation
-   Dropout
-   Batch normalization
-   Learning-rate scheduling
-   A deeper CNN architecture
-   A separate validation set
-   Confusion matrix and per-class performance analysis

## 📚 Reference

This implementation follows the concepts presented in the official
TensorFlow CNN tutorial:

https://www.tensorflow.org/tutorials/images/cnn

The original notebook contains TensorFlow documentation and
copyright/licensing information. Please retain the appropriate
attribution when redistributing or modifying the tutorial-based
material.
