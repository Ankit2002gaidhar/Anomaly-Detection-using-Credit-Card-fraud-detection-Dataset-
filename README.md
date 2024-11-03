# Credit Card Fraud Detection using RBM, VAE, and GAN

## Problem Statement
Detecting fraud in credit card transactions is critical yet challenging due to the imbalance between fraudulent and non-fraudulent transactions. This project aims to identify anomalies in transaction data to flag potential fraudulent activity using advanced anomaly detection techniques.

## Dataset
- **Name:** Credit Card Fraud Detection Dataset
- **Description:** Includes transaction data for credit card usage, containing both fraudulent and legitimate transactions.
- **Total Samples:** 284,807 transactions
- **Dataset Link:** [Credit Card Fraud Detection Dataset](https://www.kaggle.com/mlg-ulb/creditcardfraud)

## Methodology

### 1. Data Preprocessing
- **Class Balancing:** Used **SMOTE** (Synthetic Minority Over-sampling Technique) to handle the class imbalance.
- **Feature Scaling:** Applied **MinMaxScaler** for scaling data, making it compatible with the models.

### 2. Model Implementation
We implemented three models: **Restricted Boltzmann Machine (RBM)**, **Variational Autoencoder (VAE)**, and **Generative Adversarial Network (GAN)**.

#### - **Restricted Boltzmann Machine (RBM):**
   - Used for feature extraction to reduce dimensionality while retaining essential patterns of transactions.

#### - **Variational Autoencoder (VAE):**
   - Modeled transaction data to detect anomalies by reconstructing inputs; higher reconstruction errors were flagged as potential fraud.

#### - **Generative Adversarial Network (GAN):**
   - Generated synthetic transactions to augment data, improving anomaly detection robustness by training the discriminator to distinguish between real and synthetic transactions.

### 3. Evaluation Metrics
Models were evaluated based on:
- **Precision**
- **Recall**
- **F1-score**

## Selected Techniques
1. **RBM (Restricted Boltzmann Machine):**
   - Effective in capturing low-dimensional representations of high-dimensional data, aiding in anomaly detection based on transaction patterns.
  
2. **VAE (Variational Autoencoder):**
   - Learns the underlying distribution of legitimate transactions, making it suitable for identifying outliers through reconstruction errors.
  
3. **GAN (Generative Adversarial Network):**
   - Augments the dataset by generating synthetic samples, enhancing the model’s ability to detect fraudulent patterns.

## Results

- **RBM:** Successfully extracted meaningful features, enhancing the model's capability to distinguish between normal and anomalous transactions when used with downstream classifiers.
  
- **VAE:** Effectively identified anomalies using reconstruction errors as fraud indicators. Higher errors often corresponded to fraudulent transactions, highlighting discrepancies between legitimate and suspicious data patterns.
  
- **GAN:** Generated synthetic data that improved model robustness in identifying fraudulent patterns. The discriminator trained with synthetic data displayed marked improvement in detecting anomalies.

## Conclusion
The combined use of **RBM**, **VAE**, and **GAN** demonstrated strong performance in detecting anomalies within credit card transaction data. RBM improved feature extraction, VAE flagged anomalies through reconstruction errors, and GANs enhanced fraud detection accuracy by generating synthetic data. Future improvements could involve exploring hybrid models for better anomaly detection in highly imbalanced datasets.

---

