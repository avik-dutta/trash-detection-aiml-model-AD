final ai/ml project for the NVIDIA AI/ML Academy 2026

# Trash Detection AI Model:

# Garbage Classification Project

# Project Description
# This project uses a classification neural network to identify different types of trash from images. The model analyzes visual features of an object and compares them to a trained dataset to predict the type of garbage along with a confidence score. The goal is to make sorting trash easier and more accurate.

# Purpose
# The program starts with a dataset containing images of different types of trash. By analyzing the properties, angles, and visual features of objects, the model compares them to previously learned examples to find the closest match. The final output identifies the type of trash and provides the prediction accuracy to assist with waste sorting.

# Dataset Location
# CCHANGCS's **Garbage Classification** dataset on Kaggle.

# Data Split
# The dataset was manually split into training, validation, and testing folders using the `testingtraining.py` Python script.

# Neural Network
# Classification Network (ResNet-18).

# Project Development Steps
# - Found a dataset containing labeled images instead of text.
# - Selected the Garbage Classification dataset from Kaggle.
# - Downloaded the dataset using cURL.
# - Unzipped the dataset.
# - Used `testingtraining.py` to split the dataset into training, validation, and testing sets.
# - Changed directories and imported the dataset into the Jetson Inference training folder.
# - Started the Docker container.
# - Navigated to the training directory inside Docker.
# - Retrained the classification network using the training script.
# - Exported the trained model to ONNX format.
# - Exited the Docker container.
# - Set the `NET` and `DATASET` environment variables.
# - Tested the trained model using images from the dataset.

# Reproducibility
# To run this project on another machine, a NVIDIA Jetson Orin Nano with the Jetson Inference repository is required.

# Steps to Run
# 1. Connect to the Jetson Orin Nano.
# 2. Open a terminal.
# 3. Navigate to:

# cd jetson-inference/python/training/classification

# 4. Set the model variable:

# NET=models/garbagemodel1

# 5. Set the dataset variable:

# DATASET=data/Garbage-classification

# 6. Run the classifier:

# imagenet.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$DATASET/labels.txt $DATASET/test/<FOLDER>/<IMAGE>.jpg <RESULTS>.jpg

# 7. Repeat the final command with different test images as needed.

# Requirements
# - NVIDIA Jetson Orin Nano
# - Jetson Inference
# - Docker
# - Python
# - Classification training scripts
# - Garbage Classification dataset from Kaggle

# Output
# The model predicts:
# - The type of trash in the image.
# - The confidence (accuracy) of the prediction.
# - An output image displaying the classification result.
