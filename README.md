# tnsdc-genAI
# ECG Anomaly Detection using Autoencoder

This project aims to detect anomalies in electrocardiogram (ECG) signals using an autoencoder neural network. Anomalies in ECG signals can indicate various cardiac arrhythmias and other heart-related conditions. The project utilizes the MIT-BIH Arrhythmia Database for ECG data and implements the anomaly detection system in Python using the `wfdb` library and TensorFlow/Keras.

## Overview

### Data Loading and Preprocessing
- ECG data from the MIT-BIH Arrhythmia Database is loaded using the `wfdb` library.
- ECG signals are segmented into beats, and annotations for each beat are extracted.
- Different types of beats are categorized as normal, abnormal, or non-beat based on annotation symbols.

### Dataset Creation
- A dataset is created by extracting abnormal beats from the ECG signals.
- The dataset includes a specified number of seconds before and after each abnormal beat.
- The dataset is balanced by including normal beats as well.

### Data Splitting and Scaling
- The dataset is split into training and testing sets.
- Data scaling is performed using MinMaxScaler to scale the data between 0 and 1.

### Model Architecture
- Anomaly detection is performed using an autoencoder neural network.
- The autoencoder consists of an encoder and a decoder.
- The encoder compresses the input data into a lower-dimensional representation.
- The decoder reconstructs the input data from the encoded representation.

### Training
- The autoencoder is trained using the training set, where the input and output are both the normal ECG signals.
- Validation data, consisting of normal ECG signals, is used to monitor the training process and avoid overfitting.

### Evaluation
- The trained autoencoder is evaluated on both normal and anomalous (abnormal) ECG signals.
- Reconstruction errors are calculated as the differences between the input and output signals.
- The reconstruction errors are visualized to detect anomalies, where higher errors indicate anomalies.

### Visualization
- Normal and anomalous ECG signals, along with their reconstructions, are plotted to visualize the performance of the autoencoder.
- The reconstruction errors are visualized to highlight the differences between normal and anomalous signals.

## Requirements
- Python 3.x
- TensorFlow 2.x
- wfdb
- matplotlib
- pandas
- numpy
- scikit-learn
