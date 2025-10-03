# Plant Seedling Classification Using a Convolutional Neural Network

This project leverages deep learning to address a significant challenge in modern agriculture: the automated classification of plant seedlings. By building and training a Convolutional Neural Network (CNN), this model can accurately identify 12 different species of plant seedlings from images, achieving an impressive **94% accuracy** on the test set.

---

## Table of Contents

- [Project Objective](#-project-objective)
- [Dataset](#-dataset)
- [Methodology](#-methodology)
- [Model Architecture](#-model-architecture)
- [Results and Performance](#-results-and-performance)

---

## Project Objective

The goal of this project is to automate the identification of plant seedlings, reducing the need for extensive manual labor in agriculture. This AI-driven solution helps in distinguishing between crops and weeds at an early stage, which can lead to better crop yields and more sustainable farming practices.

---

## Dataset

The model was trained on a dataset from **Aarhus University**, which contains 4,750 images of plant seedlings belonging to 12 distinct species.

**List of Species:**
* Black-grass
* Charlock
* Cleavers
* Common Chickweed
* Common Wheat
* Fat Hen
* Loose Silky-bent
* Maize
* Scentless Mayweed
* Shepherds Purse
* Small-flowered Cranesbill
* Sugar beet

---

## Methodology

The project follows a comprehensive machine learning workflow:

1.  **Data Preprocessing**: The images were first cleared of noise using a Gaussian blur filter. A color-based segmentation was then applied to isolate the plants from the background.
2.  **Data Splitting**: The dataset was split into training, validation, and testing sets to ensure the model could be robustly evaluated.
3.  **Model Training**: A CNN was built from scratch using TensorFlow and Keras. It was trained for 30 epochs with a focus on maximizing validation accuracy.
4.  **Performance Evaluation**: The model's performance was measured using accuracy scores and a detailed classification report on the unseen test data.

---

## Model Architecture

A **Sequential CNN model** was designed with the following layers to effectively learn and classify the image features:

* **Convolutional Layers (`Conv2D`)**: To extract features like edges, textures, and shapes from the images.
* **Max Pooling Layers (`MaxPooling2D`)**: To reduce the dimensionality of the features and prevent overfitting.
* **Flatten Layer**: To convert the 2D feature maps into a 1D vector for the final classification stage.
* **Dense Layers**: Fully connected layers to perform the final classification, with a `softmax` activation function for multi-class output.

---

## Results and Performance

The model demonstrated excellent performance and generalization capabilities on the test set.

* **Overall Test Accuracy**: **94%**
* **Classification Report**: The model showed high precision and recall across all 12 classes, indicating its reliability in identifying each specific plant species.

This high accuracy confirms that a CNN can be a powerful and effective tool for automating plant seedling classification in real-world agricultural settings.
