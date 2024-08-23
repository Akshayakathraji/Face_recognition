###Face Recognition with PCA, LDA, and MLP
This repository contains a Python project for face recognition using Principal Component Analysis (PCA), Linear Discriminant Analysis (LDA), and a Multi-layer Perceptron (MLP) classifier. The project demonstrates how to load a dataset of face images, preprocess the images, apply dimensionality reduction techniques, and train a neural network for classification.

##Table of Contents
Installation
Usage
Dataset
Code Explanation

#Installation
Clone the repository:

git clone https://github.com/your-username/face-recognition.git
cd face-recognition
Create a virtual environment and activate it:

python -m venv env
source env/bin/activate  # On Windows use `env\Scripts\activate`
Install the required packages:

pip install -r requirements.txt

Usage
Prepare your dataset:

Place your dataset of face images in a directory named dataset/faces.
Each subdirectory in dataset/faces should correspond to a class (e.g., a person’s name), and contain the images of that class.
Run the main script:


python face_recognition.py
This script will:

Load and preprocess the images.
Apply PCA for dimensionality reduction.
Use LDA for further dimensionality reduction.
Train an MLP classifier.
Predict and evaluate the results.
Display some of the test images with predicted labels and probabilities.


##Dataset
The dataset should be organized as follows:
dataset/
    faces/
        person1/
            image1.jpg
            image2.jpg
            ...
        person2/
            image1.jpg
            image2.jpg
            ...
        ...
Make sure each subdirectory represents a unique class (e.g., an individual person).

Code Explanation
##Data Preparation:

Images are loaded from the specified directory, converted to grayscale, resized, and flattened.
Labels are assigned based on the directory names.

#Dimensionality Reduction:
PCA is used to reduce the number of features and extract principal components (eigenfaces).
LDA is applied on the PCA-transformed data to further reduce dimensionality while maximizing class separability.

#Classification:
An MLP classifier is trained on the LDA-transformed data.
The classifier’s performance is evaluated, and predictions are made on the test set.

#Visualization:
Results, including example images and their predictions, are displayed using Matplotlib.
