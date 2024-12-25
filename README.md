Airfoil Cl/Cd Prediction using Convolutional Neural Network (CNN)
This repository provides an implementation of a 6-layer Convolutional Neural Network (CNN) for predicting the aerodynamic lift-to-drag ratio (Cl/Cd) of airfoil designs. The model uses CFD-calculated Cl/Cd values as training data and demonstrates how deep learning can significantly accelerate predictions compared to traditional Computational Fluid Dynamics (CFD) software.

Features
Dataset: Uses a sample dataset 1_300.mat (airfoil figures with Cl/Cd values for 300 types of airfoils). Data includes:
data_x: A binary matrix representing the airfoil geometry.
data_y: Corresponding Cl/Cd values.
Normalization factor for scaling predictions.
Network Architecture: A well-tuned CNN with:
4 convolutional layers with Batch Normalization, ReLU activation, and MaxPooling.
2 fully connected layers for regression.
Training Details:
Trains on GPU for speed and efficiency.
Achieves a train loss of 0.06415 and validation loss of 0.36484 after 200 epochs.
Performance is 5000x faster than CFD simulations for Cl/Cd predictions.
Visualization:
Training and validation loss plotted against epochs.
Predicted vs. actual Cl/Cd values visualized for better understanding.
Confusion matrix to analyze prediction accuracy.
Repository Structure
raw_data_parsing.py: Script to parse raw airfoil data into a structured format suitable for training.
cnn_training.py: Main script to load parsed data, train the CNN model, and evaluate its performance.
Data Handling: Demonstrates how to handle train, validation, and test splits for robust performance evaluation.
Plots and Metrics:
Training/Validation loss curves.
Predicted vs. Actual Cl/Cd values.
Confusion matrix for deeper analysis.
Requirements
Python 3.7+
PyTorch
NumPy
Matplotlib
SciPy
