# 🩺 Skin Cancer Detection using Transfer Learning and Deep Learning

## 📌 Overview

This project presents a **deep learning-based skin cancer classification system** using **transfer learning techniques** on dermoscopic skin lesion images. The primary objective is to classify skin lesions into **benign** and **malignant** categories by leveraging state-of-the-art pre-trained convolutional neural networks.

Multiple transfer learning architectures were evaluated and compared to identify the most effective model for skin cancer detection. After extensive experimentation, **DenseNet121** achieved the best validation performance and was selected as the final model.

---

## 🎯 Objectives

* Develop an automated system for early skin cancer detection.
* Compare the performance of multiple transfer learning architectures.
* Identify the best-performing model for binary skin lesion classification.
* Reduce dependency on manual diagnosis and support medical decision-making.

---

## 📂 Dataset

The dataset consists of dermoscopic images categorized into:

* **Benign Skin Lesions**
* **Malignant Skin Lesions**

### Dataset Characteristics

* Balanced dataset distribution
* RGB image format
* Images resized to **224 × 224 pixels**
* Binary classification problem

---

## 🛠️ Data Preprocessing

The following preprocessing techniques were applied:

* Image resizing to **224×224**
* Data normalization
* Data augmentation using `ImageDataGenerator`
* Training and validation data generators
* Class distribution visualization

### Augmentation Techniques

* Rotation
* Zoom
* Horizontal flipping
* Width/Height shifting
* Shearing

---

## 🧠 Transfer Learning Models Evaluated

The following pre-trained CNN architectures were implemented and compared:

| Model          |
| -------------- |
| Xception       |
| ResNet50       |
| ResNet101      |
| ResNet152      |
| VGG16          |
| InceptionV3    |
| DenseNet121    |
| MobileNet      |
| MobileNetV2    |
| NASNetMobile   |
| EfficientNetB0 |
| EfficientNetB3 |
| EfficientNetB4 |

---

## 🏗️ Model Architecture

Each transfer learning model was implemented using:

* Pre-trained ImageNet weights
* Frozen convolutional backbone
* Custom classification head

### Classification Head

```text
GlobalAveragePooling2D
        ↓
Dense(1024, ReLU)
        ↓
BatchNormalization
        ↓
Dropout(0.8)
        ↓
Dense(512, ReLU)
        ↓
BatchNormalization
        ↓
Dropout(0.5)
        ↓
Dense(1, Sigmoid)
```

### Training Configuration

| Parameter         | Value               |
| ----------------- | ------------------- |
| Optimizer         | Adam                |
| Loss Function     | Binary Crossentropy |
| Image Size        | 224×224             |
| Epochs            | 150                 |
| Output Activation | Sigmoid             |
| Metric            | Accuracy            |

---

## 📊 Model Comparison Results

| Model             | Validation Accuracy |
| ----------------- | ------------------- |
| **DenseNet121**   | **86.21%**          |
| InceptionV3       | 85.30%              |
| DenseNet169       | 84.60%              |
| DenseNet201       | 84.40%              |
| InceptionResNetV2 | 84.20%              |
| EfficientNetB0    | 84.10%              |
| Xception          | 83.94%              |
| VGG16             | 83.33%              |
| VGG19             | 82.50%              |
| MobileNetV2       | 79.60%              |
| ResNet101         | 78.90%              |
| NASNetMobile      | 78.70%              |
| MobileNetV3Small  | 78.50%              |
| ResNet50          | 77.27%              |

---

## 🏆 Best Performing Model

✅ **DenseNet121**

* Validation Accuracy: **86.21%**
* Transfer learning with ImageNet weights
* Strong feature extraction capability
* Better generalization performance compared to other architectures

---

## 📈 Training Results

The final DenseNet121 model was trained for **150 epochs**, and the following metrics were monitored:

* Training Accuracy
* Validation Accuracy
* Training Loss
* Validation Loss

Performance curves were plotted to analyze:

* Model convergence
* Overfitting behavior
* Generalization capability

---

## 🧰 Technologies Used

* Python
* TensorFlow
* Keras
* NumPy
* Matplotlib
* OpenCV
* Google Colab

---



## 🚀 Future Improvements

* Fine-tuning the pretrained backbone layers
* Hyperparameter optimization
* Ensemble learning approaches
* Multi-class skin disease classification
* Explainable AI using Grad-CAM visualization
* Deployment using Streamlit/Flask

---

## 💡 Conclusion

This project demonstrates the effectiveness of **transfer learning for medical image classification**. Among several state-of-the-art CNN architectures, **DenseNet121 achieved the highest performance**, making it a promising approach for assisting in early skin cancer diagnosis.

---

## 👩‍💻 Author

**Anshika Pandey**

