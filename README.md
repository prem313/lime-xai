# ECG Image Classification with CNN and LIME Explanations

## Project Overview

This project implements an **ECG Image Classification System** using a **Convolutional Neural Network (CNN)** to classify ECG images into four categories:

1. **Normal Person ECG Images**
2. **ECG Images of Myocardial Infarction Patients**
3. **ECG Images of Patients with History of Myocardial Infarction (MI)**
4. **ECG Images of Patients with Abnormal Heartbeat**

To enhance model interpretability, **LIME (Local Interpretable Model-Agnostic Explanations)** is integrated. This helps visualize regions in ECG images that influenced the model's predictions.

---

## Features

- **Data Preprocessing**: Images are resized, normalized, and one-hot encoded.
- **CNN Architecture**: A deep learning model with Conv2D, MaxPooling, Dropout, and Dense layers.
- **Performance Evaluation**: Metrics like accuracy, confusion matrix, and classification report are provided.
- **Visualization**: 
   - Accuracy and loss curves
   - Actual vs. Predicted classes with test images
   - LIME explanations to highlight regions important for predictions.
- **Dataset Integration**: Handles both **train** and **test** image datasets.
- **Requirements Management**: Dependencies are included in `requirements.txt`.

---

## Dataset

- The dataset consists of ECG images categorized into train and test directories.
- Dataset Directory Structure:
    ```
    ECG_DATA/
    ├── train/
    │   ├── Normal Person ECG Images
    │   ├── ECG Images of Myocardial Infarction Patients
    │   ├── ECG Images of Patients with History of MI
    │   └── ECG Images of Patients with Abnormal Heartbeat
    ├── test/
    │   ├── Normal Person ECG Images
    │   ├── ECG Images of Myocardial Infarction Patients
    │   ├── ECG Images of Patients with History of MI
    │   └── ECG Images of Patients with Abnormal Heartbeat
    ```

---

## Setup Instructions

1. Install all necessary libraries using the requirements.txt file:
pip install -r requirements.txt
2. Use the dataset provided or the dataset can be downloaded froom kaggle using
   
### Download the Dataset:
To download the dataset programmatically:
```python
import kagglehub

# Download the dataset
path = kagglehub.dataset_download("evilspirit05/ecg-analysis")

print("Path to dataset files:", path)
