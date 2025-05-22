# Emotion Detection Using Fusion of Physiological Signals

This repository contains the implementation of a system for multimodal emotion detection by integrating diverse physiological signals, speech, and facial expressions within a privacy-preserving federated learning (FL) framework. The project aims to achieve robust and scalable emotion recognition in real-world scenarios.

## Overview

The core objective of this project is to accurately identify human emotions by combining information from multiple modalities. By employing a federated learning approach, the system enhances data privacy and security, as raw data remains decentralized on client devices.

## Key Features

* **Multimodal Data Fusion:** Integrates and analyzes data from:
    * **Speech:** Audio characteristics revealing emotional cues.
    * **Facial Expressions:** Visual cues from images.
    * **Physiological Signals:** Electroencephalography (EEG), Electrodermal Activity (EDA), and Photoplethysmography (PPG).
* **Federated Learning (FL) Framework:** Implements a decentralized training paradigm (e.g., FedAvg) to aggregate models from multiple clients without centralizing sensitive raw data, ensuring privacy.
* **Hybrid Model Architecture:** Employs a combination of:
    * **Long Short-Term Memory (LSTM) Networks:** For sequential speech data analysis.
    * **Convolutional Neural Networks (CNNs):** For robust facial feature extraction.
    * **Multilayer Perceptrons (MLPs):** For processing physiological signals.
    * **Attention Mechanisms:** To dynamically weight the contributions of different modalities.
* **High Performance:** Aims for high fused accuracy by effectively leveraging complementary information from multiple modalities.

## Datasets Used

The project utilizes a combination of publicly available and preprocessed datasets for training and validation:

* **CREMA-D:** A comprehensive dataset for speech emotion recognition.
* **FER-2013:** A widely used dataset for facial expression recognition.
* **PhyMER and DREAMER:** Datasets providing multimodal physiological recordings (EEG, EDA, PPG) for emotion studies.

## Technical Approach

The system involves several key steps:

1.  **Data Preprocessing:** Standardizing audio, normalizing and augmenting images, and filtering physiological signals (e.g., EEG band-pass, EDA artifact removal).
2.  **Feature Extraction:** Deriving meaningful features such as Mel-Frequency Cepstral Coefficients (MFCCs) for speech, convolutional embeddings for facial data, and Power Spectral Density (PSD) for physiological signals.
3.  **Model Training:** Training unimodal and a fused hybrid model across distributed clients within the federated learning setup.
4.  **Model Aggregation:** Utilizing federated averaging to combine client models into a robust global model while preserving data privacy.
5.  **Performance Evaluation:** Assessing the system's effectiveness using metrics like cross-validation, F1-scores, and confusion matrices.

## Potential Applications

This emotion detection system has broad applicability in various domains, including:

* Personalized intelligent assistants.
* Mental health monitoring and support systems.
* Human-computer interaction improvements.
* Customer service analytics.

## Guidance

This project was completed under the esteemed guidance of Prof. Daiwat Vyas.
