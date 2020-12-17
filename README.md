# Hand Gesture Recognition 

Hand Gesture Recognition systems involve training a machine to read our gestures using Image Processing and Machine Learning Algorithms. It is a common application in various sectors from Defence to Sensor-Based technologies. In this project we have created a model to serve this application at a basic level and checking the impact of Sobel Edge detection on the prediction results.

## Prerequisites

Dataset Used: Extract of 50 images (of any 5 gestures) [*Hand Gesture Recognition Database*](https://www.kaggle.com/benenharrington/hand-gesture-recognition-database-with-cnn)

Source: Kaggle

This project was made using [Google Colab](https://colab.research.google.com/notebooks/intro.ipynb#recent=true).

## Problem Statement

An Analysis of Edge Detection as a Feature Extractor in a Hand Gesture Recognition System based on Nearest Neighbor.

We came across the problem statement in the following [Research Paper](https://ieeexplore.ieee.org/document/6021611)

## Procedure

Algorithm used: K Nearest Neighbor (KNN)
* Pre-process: Store the image labels by stripping off parts that are not needed from image name.
* Edge Detection: Sobel operator used to create another pool of 50 edge detection images. So there are two pools of edge detected and non edge detected images.
* Logic: 
Each of the 100 images are converted to feature vectors with  raw pixel intensities by flattening them into a 1D array.
Both the datasets are split into training and testing data and fed to the 2 models created.
* Evaluation: Accuracy of both the models are calculated. A heat map is used to visualise the confusion matrix.

## Inference

* The accuracy of the classifier for without edge detected images was 80% whereas for edge detected images it was 60%. 
* For the given data sets, increasing the value of k or increasing the test size decreased the accuracy of the classifier as the dataset under consideration was quite small compared to real-world systems. Reducing the value of k or increasing the training dataset size could lead to overfitting of the model.

## Contributors

* [Trisha Sarkar](https://github.com/trishasarkar)
* [Mohit Parekh](https://github.com/mohitparekh7)
* [Samiksha Shetty](https://github.com/samiksha-18)

## Points to be Noted

* The accuracy of the model is not very high due to the following reasons -
  1. Use of raw pixel values for feature extraction - they could be influenced by intensity values.
  2. Small training data size
