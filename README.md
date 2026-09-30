# hand_writter_letter-using-CNN
# Handwritten English Letter Recognition using CNN

##Project Overview

This project uses **Deep Learning and Convolutional Neural Networks (CNN)** to recognize handwritten English letters from **A to Z**.

The model takes a handwritten letter image as input and predicts which English letter it represents.

## Objective

The main objective is to build a CNN model that can:

* Recognize handwritten English letters from **A–Z**
* Classify an image into one of **26 letter classes**
* Learn important patterns and shapes from handwritten images
* Predict letters from new handwritten images

##  Machine Learning Type

**Supervised Learning**

The model is trained using images that already have their correct letter labels.

**Example:**

* Image of `A` → Label: `A`
* Image of `B` → Label: `B`
* Image of `C` → Label: `C`

## Dataset

The dataset contains handwritten English letters from **A to Z**.

* Number of classes: **26**
* Image size: **28 × 28 pixels**
* Image type: RGB images converted to grayscale

### Preprocessing

The images are processed before training:

1. **Grayscale**
   Convert 3 color channels (RGB) into 1 grayscale channel.

2. **Normalization**
   Convert pixel values from **0–255** to **0–1**.

3. **Reshape**
   Convert the image shape from:

   `28 × 28`

   to:

   `28 × 28 × 1`

4. **Train/Test Split**
   The dataset is divided into training and testing data.

## CNN Model

The CNN model contains:

* Input layer: `28 × 28 × 1`
* Conv2D: 32 filters
* MaxPooling2D
* Conv2D: 64 filters
* MaxPooling2D
* Flatten
* Dense: 128 neurons
* Dropout: 0.3
* Output layer: 26 classes

The final layer uses **Softmax** to calculate the probability of each letter.

##  Training

The model is trained using:

* Optimizer: **Adam**
* Loss function: **Sparse Categorical Crossentropy**
* Evaluation metric: **Accuracy**
* Batch size: **64**
* Epochs: **30**

##  Results

The model achieved approximately **97.73% validation accuracy** during training.

The test accuracy can vary depending on the dataset split and training run.

The model may still make some mistakes between visually similar letters, such as:

* `D` → `O`
* `W` → `N`
* `B` → `H`

This can happen because different handwritten styles can make some letters visually similar.

## Prediction Demo

A drawing interface can be used to test the trained model.

The user can:

1. Draw an English letter.
2. Convert the drawing to the same format used during training.
3. Resize it to **28 × 28 pixels**.
4. Normalize the pixel values.
5. Send it to the CNN model.
6. Display the predicted letter.

##  Project Files

```text
handwritten-letter-recognition/
│
├── handwritten_letter_cnn.ipynb
├── handwritten_letter_cnn.keras
├── README.md
└── .gitignore
```

## Technologies Used

* Python
* TensorFlow / Keras
* NumPy
* Matplotlib
* Scikit-learn
* Google Colab
* Gradio

##  How to Run

1. Open the Jupyter notebooks in vs code 
2. Load the dataset.
3. Run the preprocessing cells.
4. Load the trained model or train the CNN.
5. Run the prediction/demo section.
6. Draw a handwritten English letter.
7. View the predicted result.

## Project Purpose

This project was created as a learning project to understand:

* Supervised learning
* Image classification
* CNN architecture
* Image preprocessing
* Model training
* Validation and testing
* Classification performance
* Real-time handwritten letter prediction
