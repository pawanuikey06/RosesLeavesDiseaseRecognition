# Rose Leaf Disease Detection

## Project Overview
This project focuses on detecting and classifying diseases in rose leaves using deep learning techniques. It employs a **Convolutional Neural Network (CNN)** model trained on a dataset containing images of rose leaves affected by different diseases. The goal is to achieve high accuracy in identifying diseased and healthy leaves.

## Features
- **Deep Learning-Based Classification**: Uses a CNN model with **ResNet50** and **SWIN Transformer** for accurate disease detection.
- **Color Space Analysis**: Experimentation with various color spaces (RGB, HSV, LAB, etc.) to improve accuracy.
- **Data Augmentation**: Techniques such as flipping, rotation, and brightness adjustment to enhance model generalization.
- **Web App Interface**: A simple UI to upload leaf images and get predictions.

---

## Dataset
### Classes
- **Black Spot** (Fungal disease)
- **Downy Mildew** (Fungal disease)
- **Fresh Leaf** (Healthy)

### Dataset Details
- **Total Images**: 4000
- **Image Resolution**: 224x224 pixels
- **Train/Test Split**: 80% training, 10% validation, 10% testing

---

## Model Architecture
### Base Model: ResNet50
- Pre-trained on **ImageNet**
- Input shape: **(224, 224, 3)**
- Fully connected layers with **softmax activation**
- Dropout layers for regularization

### SWIN Transformer
- Added for improved feature extraction
- Patch-based hierarchical architecture

### Preprocessing
- Image resizing: **128x128** for predictions
- Normalization: Pixel values scaled between **0-1**
- Data Augmentation: Rotation, zoom, flip, brightness adjustments

---

## Training Details
- **Framework**: TensorFlow / Keras
- **Optimizer**: Adam
- **Loss Function**: Categorical Crossentropy
- **Metrics**: Accuracy, Precision, Recall, F1-score
- **Epochs**: 100
- **Batch Size**: 32

**Final Results:**
| Metric  | Training  | Validation | Test |
|---------|----------|------------|------|
| Accuracy | 99.28% | 97.95% | 99.03% |
| Loss | 0.0612 | 0.1349 | 0.1538 |

---

## Installation & Usage
### Prerequisites
- Python 3.9+
- TensorFlow 2.15.0+
- Keras
- OpenCV
- NumPy, Matplotlib

### Installation
```bash
pip install -r requirements.txt
```

### Training the Model
```bash
python train.py
```

### Running the Web App
```bash
streamlit run app.py
```

---

## Future Enhancements
- **Edge Deployment**: Convert the model to **TFLite** for mobile applications.
- **Explainability**: Integrate **Grad-CAM** for model interpretability.
- **Cloud Deployment**: Deploy on **AWS Lambda** or **Google Cloud Functions**.

---

## Contributors
- **Pawan Kumar Uikey** (Lead Developer)

---

## License
This project is licensed under the **MIT License**.

---

## References
- [TensorFlow Documentation](https://www.tensorflow.org/)
- [SWIN Transformer](https://arxiv.org/abs/2103.14030)
- [ResNet50 Paper](https://arxiv.org/abs/1512.03385)

