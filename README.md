# Handwritten Digit Recognition using CNN and Semi-Supervised GAN (SGAN)

## Project Overview

Developed a deep learning framework for handwritten digit classification using the MNIST dataset. The project compares the performance of a traditional Convolutional Neural Network (CNN) trained on limited labeled data with a Semi-Supervised Generative Adversarial Network (SGAN) that leverages both labeled and unlabeled samples to improve classification performance.

The objective was to demonstrate how semi-supervised learning can enhance model accuracy when labeled data is scarce.

## Objective

Build a deep learning system that:

* Classifies handwritten digits from the MNIST dataset.
* Evaluates CNN performance on limited training data.
* Implements a Semi-Supervised GAN architecture.
* Generates synthetic handwritten digits.
* Improves classification accuracy using unlabeled data.
* Compares supervised and semi-supervised learning approaches.

## Dataset

### MNIST Handwritten Digits Dataset

* 70,000 grayscale images
* Image Size: 28 × 28 pixels
* 10 digit classes (0–9)
* Training Samples: 60,000
* Testing Samples: 10,000

## Tech Stack

* Python
* TensorFlow
* Keras
* NumPy
* Pandas
* Matplotlib
* Scikit-Learn
* Deep Learning
* GANs

## Data Preprocessing

* Normalized pixel values.
* Rescaled images between 0 and 1.
* Reshaped images for CNN input.
* Created reduced labeled datasets for semi-supervised experiments.

## Model 1: Convolutional Neural Network (CNN)

### Architecture

* Conv2D Layer
* ReLU Activation
* Max Pooling
* Dropout Layer
* Additional Convolution Layers
* Fully Connected Dense Layers
* Softmax Output Layer

### Training

* Optimizer: Adam
* Loss Function: Sparse Categorical Crossentropy
* Evaluation Metric: Accuracy

## Model 2: Semi-Supervised GAN (SGAN)

### Generator Network

The generator learns to create realistic handwritten digit images from random latent vectors.

Components:

* Dense Layers
* Reshape Layer
* Conv2DTranspose Layers
* LeakyReLU Activations
* Tanh Output Layer

### Discriminator Network

The discriminator performs two tasks:

* Distinguishes real and generated images.
* Classifies handwritten digits into 10 classes.

Components:

* Convolutional Layers
* LeakyReLU Activations
* Dropout Regularization
* Softmax Classification Layer

### GAN Architecture

The generator and discriminator are trained adversarially:

* Generator creates synthetic images.
* Discriminator evaluates authenticity.
* Classifier learns from both labeled and generated samples.

## Workflow

```text
MNIST Dataset
      │
      ▼
Data Preprocessing
      │
      ▼
CNN Baseline Model
      │
      ├── Accuracy Evaluation
      │
      ▼
Semi-Supervised GAN
      │
      ├── Generator
      ├── Discriminator
      ├── Synthetic Image Generation
      │
      ▼
Digit Classification
      │
      ▼
Performance Comparison
```

## Key Features

### CNN-Based Classification

* Handwritten digit recognition.
* Feature extraction using convolutional layers.
* Baseline supervised learning model.

### Semi-Supervised Learning

* Utilizes limited labeled samples.
* Leverages unlabeled data effectively.
* Improves learning efficiency.

### Generative Modeling

* Generates realistic handwritten digits.
* Learns latent representations of image data.
* Enhances classifier generalization.

## Evaluation Metrics

Model performance was evaluated using:

* Classification Accuracy
* Training Loss
* Validation Loss
* Digit Prediction Performance

## Results

* Successfully implemented CNN-based digit classification.
* Developed a Semi-Supervised GAN architecture.
* Demonstrated the effectiveness of SGAN when labeled data is limited.
* Generated realistic handwritten digit images.
* Improved classification capability through adversarial training.

## Applications

* Optical Character Recognition (OCR)
* Document Digitization
* Postal Code Recognition
* Banking and Check Processing
* Educational AI Systems
* Semi-Supervised Learning Research

## Future Improvements

* Apply SGAN to more complex datasets such as CIFAR-10.
* Implement Conditional GANs (CGAN).
* Compare with Variational Autoencoders (VAE).
* Deploy as an interactive web application.
* Explore advanced GAN architectures such as StyleGAN and DCGAN.

## Author

**Deepti Verma**

GitHub: [https://github.com/Deep4verma/]

LinkedIn: [https://www.linkedin.com/in/deeptiverma1004/]
