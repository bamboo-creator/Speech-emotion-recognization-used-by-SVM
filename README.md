# 🎙️ Speech-emotion-recognization-used-by-SVM

This project implements a **Speech Emotion Recognition (SER)** system using a **Support Vector Machine (SVM)** classifier with a **Radial Basis Function (RBF)** kernel. The goal is to classify spoken utterances into seven discrete emotional categories based on acoustic features. The model is trained on MFCC features extracted from a combination of emotional speech datasets, demonstrating robust performance in detecting emotions such as **fearful**, **neutral**, and **angry**.

---

## 📌 Emotion Classes

The model is trained to recognize the following seven emotions:

- 😠 Angry  
- 🤢 Disgust  
- 😨 Fearful  
- 😊 Happy  
- 😐 Neutral  
- 😢 Sad  
- 😲 Surprised  

---

## 📁 Dataset

This project uses a combined dataset constructed from three widely used emotional speech corpora:

- [RAVDESS](https://zenodo.org/record/1188976) (Ryerson Audio-Visual Database of Emotional Speech and Song)
- [SAVEE](https://www.kaggle.com/datasets/balabaskar/surrey-audiovisual-expressed-emotion-savee)
- [TESS](https://tspace.library.utoronto.ca/handle/1807/24487)

Each dataset provides high-quality recordings from multiple speakers expressing various emotions in English.

> ⚠️ **Note**: Due to file size limitations on GitHub, the full dataset is not included in this repository.

📦 **Download the full dataset**: [Google Drive Link](https://your-google-drive-link-here](https://drive.google.com/drive/folders/1XFC5Pk9o9wadCy9fHSXxS12lpujyBQb2?usp=drive_link)

Alternatively, a small subset of the data for quick testing is included in the `data_sample/` folder (if available).

---

## 🔧 Features & Methods

- 📌 **Feature Extraction**:  
  - 40-dimensional **Mel-Frequency Cepstral Coefficients (MFCCs)**
  - Per-frame feature extraction using `librosa`

- ⚙️ **Model**:  
  - **SVM classifier with RBF kernel**
  - Trained on extracted MFCCs
  - Balanced across classes

- 📈 **Evaluation Metrics**:
  - Accuracy
  - Precision, Recall, F1-score
  - Confusion Matrix
  - ROC Curve (One-vs-Rest AUC)
  - t-SNE Visualization of Feature Space

---

## 📊 Results Summary

| Metric                | Value     |
|-----------------------|-----------|
| Overall Accuracy      | **70%**   |
| Best Recognized Emotions | Fearful, Neutral, Angry |
| Most Confused Emotions | Happy, Disgust, Surprised |

- **F1-score (Fearful)**: 0.78  
- **F1-score (Disgust)**: 0.64  
- **Macro Avg F1-score**: 0.70  

Visualizations included:
- ✅ Confusion Matrix  
- ✅ t-SNE Feature Clustering  
- ✅ ROC Curve (per class AUC ≥ 0.89)

---



