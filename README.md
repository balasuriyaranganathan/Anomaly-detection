# Anomaly Detection using Autoencoders

This project demonstrates the use of autoencoders for detecting anomalies in network data. An autoencoder is a type of artificial neural network used for dimensionality reduction and anomaly detection.

## Project Overview

The project aims to identify anomalies in network data using an autoencoder-based approach. Anomalies, in this context, refer to network congestion points or unusual patterns that deviate from normal behavior.

## Project Steps

1. **Import Required Libraries**
2. **Read and Load Data**
3. **Data Preprocessing**
4. **Label Encoding**
5. **Feature Scaling**
6. **Define Autoencoder Model**
7. **Compile Model**
8. **Train Autoencoder**
9. **Anomaly Detection**
10. **Identify Congestion Points**

## Code Explanation

The project performs the following steps:

1. Required libraries, including pandas, numpy, and TensorFlow's Keras, are imported.
2. Data is read from a CSV file using pandas.
3. The 'Protocol' and 'Length' columns are extracted as features.
4. The 'Protocol' column is label encoded using the LabelEncoder from scikit-learn.
5. Data is scaled using MinMaxScaler to ensure all features are on the same scale.
6. An autoencoder model is defined using Sequential API from Keras.
7. The model consists of two Dense layers representing the encoding and decoding parts of the autoencoder.
8. The model is compiled with 'adam' optimizer and 'mean_squared_error' loss function.
9. The autoencoder is trained using the scaled data as both input and output for a certain number of epochs.
10. Anomaly scores (MSE) are calculated by comparing original data with reconstructed data.
11. A threshold for anomaly detection is determined using a percentile of the MSE scores.
12. Network data corresponding to anomaly scores above the threshold are identified as congestion points.

## Usage and Interpretation

This project can be applied to network monitoring scenarios to identify congestion points or anomalies. By comparing the MSE scores to a threshold, unusual network behavior can be detected and further investigated.

## Adjustments

Depending on your data and requirements, you might need to adjust:

- Features used
- Encoding dimension
- Threshold percentile
- Model hyperparameters

## Conclusion

Using autoencoders for anomaly detection can be effective in identifying unusual patterns in network data. This project showcases the process of preparing data, building an autoencoder, and utilizing anomaly scores to detect congestion points. Adapt and fine-tune the approach to your specific use case for accurate anomaly detection.

## Dataset Description

Here's a description of the columns in my dataset:

Time: The time when the network event occurred. It could be measured in seconds or milliseconds, depending on the data source.

Source: The source IP address or hostname of the network communication.

Destination: The destination IP address or hostname of the network communication.

Protocol: The protocol used for the communication, such as TCP, ARP, etc.

Length: The length of the packet or message exchanged during the communication.

Info: Additional information or details about the communication event.

