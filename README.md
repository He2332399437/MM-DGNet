# MM-DGNet
Multimodal Domain Generalization for Cross-Condition Inter-Turn Short-Circuit Diagnosis in Permanent Magnet Synchronous Motors
Introduction

This project handles three-channel current signal data and involves feature extraction and fault diagnosis tasks for mechanical equipment vibrations. The project includes modules for data processing, model training, and evaluation, with the goal of performing fault detection through multimodal feature fusion.

Environment Requirements

To ensure the project runs smoothly, please make sure the required Python libraries are installed. You can either use requirements.txt or manually install the following libraries to ensure that your environment contains all necessary dependencies.

File Descriptions

dataset.py
Data processing file. This code implements a complete data processing pipeline for three-channel CSV-format mechanical equipment vibration data, including:

Loading data from raw CSV files

Data preprocessing (e.g., normalization, denoising, etc.)

Feature extraction

Dataset splitting (training set, validation set, test set)

This file is the core of data processing, ensuring that the data is processed in a format suitable for model training.

CEPM.py
This file implements Cross-Condition Evolution Prior Modeling (CEPM), which dynamically generates evolution samples. It solves the problem of insufficient samples for certain categories and single domain distribution by generating synthetic data for each category, enhancing the diversity of the training set and improving the model's generalization capability.

model.py
Model parameter file. This file defines the model architecture and uses a lightweight attention mechanism (such as a simplified Transformer structure). By reducing the model depth and embedding dimensions, it ensures a balance between computational efficiency and performance, allowing the model to respond quickly in real-time applications.

train.py
Training file. This file contains the implementation of the training process, including:

Data loading

Model training

Loss function and optimizer settings

Training log recording (e.g., training loss, accuracy, etc.)

Model saving

This file is the entry point for the entire training process, and you can start the training by running it.

test.py
Testing file. This file is responsible for evaluating the trained model, mainly implementing:

Loading the trained model

Inference and evaluation on the test set

Outputting performance metrics (e.g., accuracy, F1 score, etc.)

This file is used to validate the model's performance on unseen data.

File Status

The above files are still being organized and refined. Some features may not be fully uploaded or are still under development. The full code and detailed documentation will be updated and supplemented in the future.
