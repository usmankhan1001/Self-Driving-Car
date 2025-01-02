Self-Driving Car Project using NVIDIA CNN Model

Overview

This project implements an end-to-end deep learning pipeline for autonomous driving using NVIDIA's CNN architecture. The model predicts steering angles directly from raw images captured by a car’s front-facing camera. It focuses on preprocessing, feature extraction, and decision-making to enable robust self-driving behavior.

Features

 
End-to-End Learning: Direct mapping from images to steering commands.
Preprocessing: Cropping, resizing, YUV color conversion, and data augmentation for improved model performance.
NVIDIA CNN Architecture: Convolutional layers for feature extraction and fully connected layers for decision-making.
Batch Processing: Optimized memory usage during training for large datasets.
Data Augmentation: Techniques like zooming, brightness adjustment, panning, and flipping for dataset diversity.
Technologies Used
Languages: Python
Frameworks and Libraries:
TensorFlow/Keras (for building and training the CNN model)
NumPy (numerical computations)
Pandas (data manipulation and analysis)
OpenCV (image processing)
Matplotlib (data visualization)
Architecture
Input:
Preprocessed images of 200x66 pixels in YUV color format.
Convolutional Layers:
5 layers with progressively increasing filters (24, 36, 48, 64, 64).
Kernel sizes: 
5×5
5×5 for initial layers, 
3×3
3×3 for deeper layers.
Strides: 
2×2
2×2 for downsampling and 
1×1
1×1 for fine details.
Flatten Layer:
Converts 2D feature maps into a 1D vector.
Fully Connected Layers:
Three layers with 100, 50, and 10 neurons, respectively, leading to the final steering angle prediction.
How It Works
Data Loading:
Load images and corresponding steering angles from a GitHub repository.
Preprocessing:
Crop irrelevant parts (sky, hood).
Resize images to 200x66 pixels.
Convert to YUV color format.
Normalize pixel values.
Data Augmentation:
Simulate real-world variations with zooming, brightness changes, panning, and flipping.
Model Training:
Batch generator used for efficient memory management.
Trained using mean squared error (MSE) loss function.
Prediction:
Outputs a single steering angle based on the input image.
