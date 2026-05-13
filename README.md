# GrayScale-Histogram-Equalization
## OpenCV Histogram Equalization for Image Enhancement

A Python-based image processing experiment that demonstrates Histogram Equalization using OpenCV to enhance the contrast of grayscale images.

This project reads a grayscale image, analyzes its histogram distribution, applies histogram equalization, and displays the results using Matplotlib.

## Objective

## The objective of this experiment is to:

Understand histogram equalization in digital image processing.
Improve image contrast using OpenCV.
Compare original and enhanced grayscale images.
Visualize histogram distribution before and after equalization.
## Technologies Used
Python

OpenCV (cv2)

NumPy

Matplotlib


## Project Structure
├── parrot.jpg

├── histogram_equalization.py

├── Histogram.ipynb

└── README.md


## Requirements

Install the required libraries using:

pip install opencv-python numpy matplotlib
Program Description

## The program performs the following steps:

Imports required libraries.
Reads the image parrot.jpg in grayscale mode.
Displays the original grayscale image.
Plots the histogram of the original image.
Applies histogram equalization using:
cv2.equalizeHist()
Displays the enhanced image.
Plots the histogram of the equalized image.
Uses a 2 × 2 grid layout for visualization.
Sample Python Code
import cv2
import numpy as np
import matplotlib.pyplot as plt


# Read image in grayscale
```py
img = cv2.imread('parrot.jpg', 0)
```

# Histogram Equalization
```py
equalized = cv2.equalizeHist(img)
```

# Display results
```py
plt.figure(figsize=(10,8))


plt.subplot(2,2,1)
plt.imshow(img, cmap='gray')
plt.title('Original Image')
plt.axis('off')


plt.subplot(2,2,2)
plt.hist(img.ravel(), 256, [0,256])
plt.title('Original Histogram')


plt.subplot(2,2,3)
plt.imshow(equalized, cmap='gray')
plt.title('Equalized Image')
plt.axis('off')


plt.subplot(2,2,4)
plt.hist(equalized.ravel(), 256, [0,256])
plt.title('Equalized Histogram')


plt.tight_layout()
plt.show()
```

## Result

The histogram equalization process successfully enhanced the contrast of the grayscale image. After applying cv2.equalizeHist(), the intensity values were redistributed more uniformly across the histogram range, making the image details clearer and visually improved.
