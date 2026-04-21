# Group13-55-710603-SematicSegmentation

# Title :
# Comparative Water Body Mapping Using Multiple Deep Learning Semantic Segmentation Models on Satellite Imagery
# Domain : Computer Vision and Deep Learning 

# Team Details
Salva Muskan
Role: Documentation and Presentation Lead
Student ID: c5057947

# Project Overview

This project focuses on semantic segmentation of water bodies from satellite images using deep learning models. The objective is to classify each pixel in a satellite image as water or non-water.

# Models used:
Simple U-Net
Fully Convulutional Neural Network (FCN)
Attention Residual U-Net
DeepLabV3  

# Dataset
Dataset used:
Satellite Images of Water Bodies
# Dataset link:
https://www.kaggle.com/datasets/franciscoescobar/satellite-images-of-water-bodies
Dataset details:

Total images: 2841
Image size: 256 x 256 x 3
Mask size: 256 x 256 x 1

Note: The dataset is uploaded to Google Drive for easy access in Colab.


# Environment Setup

Create a file named requirements.txt:

tensorflow
numpy
matplotlib
seaborn
scikit-learn

# Install dependencies:

pip install -r requirements.txt

If using Google Colab, no installation is required.


# How to Run the Project

This project uses a single script for execution.

Step 1: Clone the repository

git clone <your-repo-link>
cd <your-repo-folder>

Step 2: Install dependencies

pip install -r requirements.txt

Step 3: Run the project

python Semantic_Segmentation_Demo_Code.py

This script will:

Load dataset (from Google Drive or local path)
Preprocess images (resizing and normalization)
Load the pretrained model
Perform segmentation on input images
Display predicted masks


# Running in Google Colab

Step 1: Upload the following to Google Drive:

Dataset folder
Trained model (model.h5)
Semantic_Segmentation_Demo_Code.py

Step 2: Open Google Colab and run:

from google.colab import drive
drive.mount('/content/drive')

Step 3: Run the script in Colab:

!python /content/drive/MyDrive/your-folder/Semantic_Segmentation_Demo_Code.py
Training Configuration
Batch size: 8
Epochs: 20
Optimizer: Adam
Loss function: Binary Cross Entropy + Dice Loss

Metrics used:

Accuracy
IoU
Dice Coefficient
F1-score



# Results
Model	Accuracy	IoU	Dice	F1-score
Simple U-Net	0.8420	0.5742	0.7280	0.7280
FCN	0.7737	0.4234	0.5921	0.5921
DeepLabV3 Lite	0.7856	0.5079	0.6718	0.6718
Attention-ResUNet	0.8727	0.6600	0.7939	0.7939

# Best model: Attention Residual U-Net

# Project Structure
project/
│── Semantic_Segmentation_Demo_Code.py
│── requirements.txt
│── README.md
│── water_segmentation_model.h5
│── Water Bodies Dataset/
Conclusion

This project demonstrates that deep learning models can effectively perform pixel-level segmentation of water bodies from satellite imagery. The Attention Residual U-Net achieved the best performance due to improved feature learning using residual connections and attention mechanisms.

The approach is scalable and suitable for real-world applications such as environmental monitoring and flood detection.
