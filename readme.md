# 🍅 Tomato Disease Classification using Deep Learning

[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.15.0-orange?logo=tensorflow)](https://tensorflow.org)
[![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python&logoColor=white)](https://python.org)
[![Accuracy](https://img.shields.io/badge/Accuracy-99.21%25-success)](#model-performance)

## 📋 Overview
A deep learning model to classify tomato leaf diseases into three categories:
- Early Blight
- Late Blight
- Healthy

## 🔍 Dataset
- Total images: 4496 across 3 classes
- Image size: 256x256 pixels
- RGB channels: 3
- Batch size: 32

## 🛠 Model Architecture
```python
Sequential([
    # Input preprocessing
    Resize and Rescale Layer
    Data Augmentation Layer
    
    # Convolutional layers
    Conv2D(32, (3,3), activation='relu')
    MaxPooling2D(2,2)
    Conv2D(64, (3,3), activation='relu')
    MaxPooling2D(2,2)
    # Multiple Conv2D layers with similar structure
    
    # Output layers
    Flatten()
    Dense(64, activation='relu')
    Dense(3, activation='softmax')  # 3 classes
])
```

## 🎯 Model Performance
- Training Accuracy: 98.71%
- Validation Accuracy: 99.33%
- Test Accuracy: 99.21%
- Final Loss: 0.0319

## 🔄 Data Preprocessing
- Image resizing to 256x256
- Rescaling pixel values to [0,1]
- Data augmentation:
  - Horizontal and vertical flips
  - Random rotation (0.2)

## 📊 Training Details
- Epochs: 100
- Steps per epoch: 112
- Batch size: 32
- Training time per step: ~6s

## 📈 Results Visualization
The model shows excellent convergence with:
- Steady increase in accuracy
- Consistent decrease in loss
- No significant overfitting

## 🚀 Requirements
```bash
pip install tensorflow
pip install numpy
pip install matplotlib
```

## 📝 Usage
1. Clone the repository
2. Install dependencies
3. Place your tomato leaf images in the appropriate directory
4. Run the model for classification

## 🏆 Performance Metrics
```
Final Metrics:
- Loss: 0.0319
- Accuracy: 98.75%
```

---
<div align="center">
    <b>Built with 🤖 TensorFlow and ❤️</b>
</div>
