# Cyber Attack Detection Using Machine Learning

## Project Overview

This project explores the use of Machine Learning and Deep Learning techniques to detect and classify cyber attacks based on network traffic characteristics.

Using the CIC-IDS2017 dataset, the project analyses network traffic and classifies it into benign traffic and different categories of cyber attacks.

Two classification approaches are implemented and compared:

- **Random Forest** – An ensemble machine learning algorithm used for multi-class network attack classification.
- **1D Convolutional Neural Network (CNN)** – A deep learning model designed to identify patterns in preprocessed network traffic features.

The objective is to evaluate both approaches and understand their effectiveness in identifying different types of network attacks.

## Technologies Used

- Python
- Pandas & NumPy
- Scikit-learn
- TensorFlow / Keras
- Matplotlib
- Seaborn
- Google Colab

## Dataset

The project uses the **CIC-IDS2017 dataset**, which contains network traffic data representing benign activities and various cyber attacks.

Dataset source: [CIC-IDS2017 – Hugging Face](https://huggingface.co/datasets/c01dsnap/CIC-IDS2017)

The notebook automatically downloads eight CSV files from a public Hugging Face dataset mirror.

### Attack Categories

The notebook groups the original traffic labels into the following categories:

- Benign
- DDoS
- DoS
- PortScan
- Bot
- Brute Force
- Web Attack
- Infiltration
- Other (fallback category)

## Project Workflow

### 1. Data Collection
- Download eight CIC-IDS2017 CSV files.
- Combine the datasets into a single DataFrame.
- Inspect network traffic records and available features.

### 2. Data Cleaning
- Handle infinite values.
- Remove missing values.
- Group original attack labels into standard attack categories.
- Visualise the distribution of traffic classes.

### 3. Data Preprocessing
- Downsample the dominant Benign traffic category to manage dataset size.
- Separate features and classification labels.
- Apply One-Hot Encoding to categorical features.
- Standardise numerical features.
- Split the dataset into training and testing sets.

### 4. Principal Component Analysis (PCA)
- Apply PCA to explore dimensionality reduction.
- Analyse cumulative explained variance.
- Visualise the contribution of principal components.

### 5. Random Forest Classification
- Train a Random Forest classifier with 200 estimators.
- Apply balanced class weighting.
- Perform multi-class attack classification.
- Analyse feature importance.
- Generate a confusion matrix and classification report.

### 6. Deep Learning – 1D CNN
- Reshape the preprocessed network traffic features.
- Build a 1D CNN architecture using TensorFlow/Keras.
- Apply convolutional layers, batch normalisation and max pooling.
- Use dropout to help reduce overfitting.
- Implement early stopping during training.
- Evaluate model performance on the test dataset.

### 7. Model Evaluation & Comparison

Both models are evaluated using:

- Accuracy
- Precision (Macro)
- Recall (Macro)
- F1-score (Macro)
- Confusion Matrix
- Classification Report
- Precision-Recall Curves

A final comparison table and visualisation are generated to compare the performance of Random Forest and 1D CNN.

## How to Run

The notebook is designed to run using **Google Colab**.

1. Open the notebook in Google Colab.
2. Select Runtime → Change runtime type.
3. Select GPU (optional, recommended for CNN training).
4. A High-RAM runtime is recommended due to the dataset size.
5. Run all cells from top to bottom.

**Note:** The notebook automatically downloads all eight dataset files. No manual dataset upload is required.

## Repository Structure

```text
Cyber-Attack-Detection-Using-Machine-Learning/
│
├── 2_Cyber_Attack_Detection.ipynb
└── README.md
```

## Learning Outcomes

This project demonstrates practical implementation of:

- Network intrusion detection concepts.
- Network traffic analysis.
- Machine Learning for cybersecurity.
- Deep Learning using 1D CNN.
- Multi-class classification.
- Feature preprocessing and dimensionality reduction.
- Model performance evaluation.
- Comparative analysis of traditional ML and Deep Learning approaches.

## Disclaimer

This project is developed for educational and research purposes as part of cybersecurity studies. The models demonstrate machine learning approaches to network attack classification and are not intended to replace production-grade intrusion detection and prevention systems.

---

**Project Area:** Cybersecurity | Network Security | Machine Learning | Deep Learning | Network Intrusion Detection
