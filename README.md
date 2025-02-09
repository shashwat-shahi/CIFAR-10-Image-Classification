# CNN Architecture for CIFAR-10

This repository contains different Convolutional Neural Network (CNN) architectures designed to classify images from the CIFAR-10 dataset. The models incorporate various techniques to improve accuracy and prevent overfitting.

## 📌 Dataset
CIFAR-10 consists of 60,000 32x32 color images in 10 classes, with 6,000 images per class.

## 🏗️ Model Architectures

### **Model 1**
- **Layers:**
  - Conv2D (32 filters, 3x3, ReLU)
  - MaxPooling2D (2x2)
  - Conv2D (64 filters, 3x3, ReLU)
  - MaxPooling2D (2x2)
  - Conv2D (64 filters, 3x3, ReLU)
  - Flatten
  - Dense (64 units, ReLU)
  - Output: Dense (10 units, softmax)
- **Overfitting Prevention:** Data Augmentation, Dropout, L2 Regularization

### **Model 2**
- **Enhancements Over Model 1:**
  - L2 Regularization added to Conv2D and Dense layers
  - Dropout layers (25% and 50%) added for better generalization
- **Underfitting Prevention:** Adding more layers

### **Model 3**
- **Advanced Architecture:**
  - Multiple Conv2D layers (64, 128, 256 filters) with Batch Normalization
  - MaxPooling2D after each convolution block
  - Dropout layers (20%, 30%, 40%, 50%) for better regularization
  - Dense (512 units) with L2 Regularization and Batch Normalization
  - Output: Dense (10 units, softmax)

## 🚀 How to Run
1. Install dependencies:
   ```bash
   pip install tensorflow keras numpy matplotlib
   ```
2. Train the model:
   ```python
   python train.py
   ```
3. Evaluate the model:
   ```python
   python evaluate.py
   ```

## 🔍 Results & Observations
- Model 3 provides the best performance due to batch normalization and deeper architecture.
- Overfitting is handled using Dropout and L2 Regularization.
- Adding more layers improves model capacity and prevents underfitting.

## 📧 Contact
Developed by **Shashwat Shahi**  
📩 shahi.sh@northeastern.edu
