# tnsdc-genAI
# ECG Anomaly Detection using Autoencoder

## Overview

This project focuses on detecting anomalies in electrocardiogram (ECG) signals using an autoencoder neural network. An autoencoder is a type of artificial neural network used for unsupervised learning. In this project, the autoencoder is trained on normal ECG signals and aims to reconstruct them accurately. Anomalies are then detected by comparing the reconstruction error between normal and abnormal signals.

## Dataset

The dataset used in this project is the MIT-BIH Arrhythmia Database. It consists of ECG recordings from 48 subjects, each containing various types of heartbeats annotated with symbols indicating normal beats and different types of abnormal beats.

## Project Structure

- **data_processing.ipynb**: Jupyter Notebook containing code for data preprocessing, including reading ECG signals, extracting beats, and creating datasets for training and testing.
- **model_training.ipynb**: Jupyter Notebook containing code for building and training the autoencoder model using TensorFlow/Keras.
- **results_analysis.ipynb**: Jupyter Notebook for analyzing the performance of the trained model and visualizing reconstruction errors.
- **requirements.txt**: File listing all Python packages required to run the code.
- **README.md**: This file, providing an overview of the project.


## Usage

1. **Data Preprocessing**: Run `data_processing.ipynb` to preprocess the ECG data and create datasets for training and testing.
2. **Model Training**: Execute `model_training.ipynb` to build and train the autoencoder model.
3. **Results Analysis**: Utilize `results_analysis.ipynb` to evaluate the performance of the trained model and visualize reconstruction errors.

## Results

The trained autoencoder model achieves a high accuracy in reconstructing normal ECG signals. Anomalies are detected based on significant deviations between the original signals and their reconstructions.

## Acknowledgments

- The MIT-BIH Arrhythmia Database for providing the ECG dataset used in this project.
- TensorFlow and Keras libraries for building and training neural networks.

## Requirements

All required Python packages are listed in the `requirements.txt` file. You can install them using the following command:

```bash
pip install -r requirements.txt
# ECG Anomaly Detection using Autoencoder
