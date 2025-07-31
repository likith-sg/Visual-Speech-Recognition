# Visual Speech Recognition (Lip Reading)

This repository presents a Visual Speech Recognition system that performs lip reading using silent video sequences. The model is built using a 3D Convolutional Neural Network (3D CNN) to classify short video clips into spoken word categories by analyzing spatio-temporal patterns in lip movements.

## Objective

The objective of this project is to explore deep learning methods for recognizing spoken words without using audio data. By leveraging 3D convolutional networks, the system learns to extract meaningful visual features across both spatial and temporal dimensions of video frames. This approach can be applied in areas such as silent communication interfaces, assistive technologies for the hearing impaired, and speech recognition in noisy environments.

## Methodology

The model is trained on a labeled dataset of silent video clips, where each sample corresponds to a person speaking a specific word. The raw video data is preprocessed into frame arrays and normalized. Labels are encoded into numerical form for classification.

A 3D CNN is used as the core architecture, designed to capture both spatial (lip shape and position) and temporal (movement over time) features. The model includes multiple convolutional and pooling layers, followed by fully connected layers with dropout for regularization. The final layer uses softmax activation to predict the spoken word.

The model is trained using categorical crossentropy loss and evaluated using classification metrics such as precision, recall, and F1-score. Inference results on random test samples are visualized along with the corresponding frame sequences to demonstrate model behavior.

## Dataset Credit

The dataset used in this project is the Best Lip Reading Dataset, publicly available on Kaggle:

[https://www.kaggle.com/datasets/allenye66/best-lip-reading-dataset](https://www.kaggle.com/datasets/allenye66/best-lip-reading-dataset)

It consists of silent video recordings of individuals speaking one of thirteen predefined words. Each video is stored as a sequence of frames in structured directories. The dataset provides a challenging benchmark for visual-only speech recognition.
