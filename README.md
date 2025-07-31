# Visual Speech Recognition (Lip Reading)

Visual Speech Recognition system that performs lip reading using silent video sequences. The model is built using a 3D Convolutional Neural Network (3D CNN) to classify short video clips into spoken word categories by analyzing spatio-temporal patterns in lip movements.

## Objective

The objective of this project is to explore deep learning methods for recognizing spoken words without using audio data. By leveraging 3D convolutional networks, the system learns to extract meaningful visual features across both spatial and temporal dimensions of video frames. This approach can be applied in areas such as silent communication interfaces, assistive technologies for the hearing impaired, and speech recognition in noisy environments.

## Methodology

The model is trained on a labeled dataset of silent video clips, where each sample corresponds to a person speaking a specific word. The raw video data is preprocessed into frame arrays and normalized. Labels are encoded into numerical form for classification.

A 3D CNN is used as the core architecture, designed to capture both spatial (lip shape and position) and temporal (movement over time) features. The model includes multiple convolutional and pooling layers, followed by fully connected layers with dropout for regularization. The final layer uses softmax activation to predict the spoken word.

The model is trained using categorical crossentropy loss and evaluated using classification metrics such as precision, recall, and F1-score. Inference results on random test samples are visualized along with the corresponding frame sequences to demonstrate model behavior.

## Dataset Credit

The dataset used in this project is the Best Lip Reading Dataset, publicly available on Kaggle:

[https://www.kaggle.com/datasets/allenye66/best-lip-reading-dataset](https://www.kaggle.com/datasets/allenye66/best-lip-reading-dataset)

# Instructions

To run this project end-to-end, follow the steps below:

1.  **Clone the Repository to Your Local Machine**
    ```bash
    git clone https://github.com/likith-sg/Visual-Speech-Recognition.git
    ```

2.  **Open Google Colab**
    Navigate to Google Colab and upload the `preliminary.ipynb` notebook from the cloned repository.

3.  **Upload Your `kaggle.json` API Key**
    - Go to your Kaggle Account Settings.
    - Scroll to the API section and click on `Create New API Token`.
    - Save the downloaded `kaggle.json` file to your local system.
    - In the first cell of the notebook, upload the key using:
      ```python
      from google.colab import files
      files.upload()  # Upload kaggle.json
      ```

4.  **Run All Cells Sequentially**
    - Click `Runtime` > `Run all` to execute the notebook.
    - For optimal performance, select `T4 GPU` via `Runtime` > `Change runtime type`.
