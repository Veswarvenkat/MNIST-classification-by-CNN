# MNIST Handwritten Digit Classification using CNN

This project implements a Convolutional Neural Network (CNN) using TensorFlow and Keras to classify grayscale images of handwritten digits (0 through 9) from the widely-used MNIST dataset.

## Project Overview

The notebook covers the essential steps for building and training an image classifier:
* **Data Loading:** Loads the standard MNIST dataset included with Keras.
* **Preprocessing:**
    * Reshapes the images to include a channel dimension (`28x28x1`) suitable for CNN input.
    * Normalizes pixel values from the 0-255 range to the 0-1 range.
    * **One-hot encodes** the integer labels (0-9) into a categorical format (e.g., `5` becomes `[0,0,0,0,0,1,0,0,0,0]`).
* **Model Building:** Defines a `Sequential` CNN model with convolutional, pooling, and dense layers.
* **Training:** Trains the model on the MNIST training data, using a portion for validation.
* **Evaluation:** Measures the trained model's accuracy on the unseen test dataset.
* **Visualization:** Plots the training and validation accuracy over epochs and shows a sample prediction.

---

## Dataset: MNIST Handwritten Digits

* **Source:** `tensorflow.keras.datasets.mnist`
* **Content:** Grayscale images of handwritten digits.
* **Size:** 60,000 training images, 10,000 testing images.
* **Dimensions:** Each image is 28x28 pixels.
* **Classes:** 10 (digits 0 through 9).


---

## Model Architecture

The model is a `Sequential` CNN built with the following layers:

1.  **Conv Block 1:**
    * `Conv2D` (32 filters, 3x3 kernel, `relu` activation, input_shape=(28, 28, 1))
    * `MaxPooling2D` (
