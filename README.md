# MNIST-GAN-digit-generator
A Generative Adversarial Network (GAN) built using TensorFlow/Keras to generate handwritten digit images similar to the MNIST dataset, demonstrating adversarial learning and generative modeling.


# 🧠 MNIST Digit Generation using GAN (TensorFlow/Keras)

## 📌 Project Overview

This project implements a Generative Adversarial Network (GAN) using TensorFlow (Keras API) to generate handwritten digit images similar to the MNIST dataset. The goal is to understand adversarial learning and how generative models can learn data distributions.

---

## 🎯 Objective

To build and train a GAN model that can generate realistic handwritten digit images from random noise using deep learning techniques.

---

## 📊 Dataset

* Source: TensorFlow MNIST Dataset
* Total Images: 60,000 (training)
* Image Size: 28×28 grayscale
* Preprocessing:

  * Normalized pixel values to range [-1, 1]
  * Reshaped to (28, 28, 1)

---

## ⚙️ Model Architecture

### 🔹 Generator Network

* Input: 100-dimensional random noise vector
* Layers:

  * Dense → BatchNormalization → LeakyReLU
  * Reshape → Conv2DTranspose layers
  * Output layer with **Tanh activation**
* Output: 28×28 generated image

---

### 🔹 Discriminator Network

* Input: Real or generated image
* Layers:

  * Conv2D → LeakyReLU → Dropout
  * Flatten → Dense
  * Output layer with **Sigmoid activation**
* Output: Probability (Real = 1, Fake = 0)

---

## 🧠 Training Details

* Loss Function: Binary Cross-Entropy (BCE)
* Optimizer: Adam

  * Learning Rate = 0.0002
  * Beta1 = 0.5
* Epochs: 20
* Batch Size: 256

### 🔁 Training Process

1. Generate fake images using Generator
2. Train Discriminator on real and fake images
3. Train Generator to fool Discriminator
4. Repeat for multiple epochs

---

## 📈 Results

### 🖼️ Generated Images

* Initial epochs produce noisy images
* Gradually, recognizable digit patterns emerge
* Image quality improves over time

---

### 📊 Loss Curves

* Generator and Discriminator losses fluctuate
* This is expected due to adversarial training
* Indicates both models are learning simultaneously

---

## 🔍 Observations

* GAN training is unstable compared to traditional models
* Generator improves gradually in producing realistic digits
* Discriminator maintains balance in classification
* Loss does not follow a simple decreasing trend

---

## ⚠️ Challenges Faced

* Training instability
* Mode collapse (repeated digit generation)
* Slow training due to dual model updates
* Plotting and visualization issues

---

## 🚀 Future Improvements

* Train for more epochs for better image quality
* Use advanced architectures like DCGAN
* Tune hyperparameters
* Save generated images across epochs

---

## 🛠️ Tech Stack

* Python
* TensorFlow / Keras
* NumPy
* Matplotlib

---


## 📌 Conclusion

This project demonstrates the implementation of a GAN model capable of generating handwritten digits. It highlights the concept of adversarial learning and showcases how deep learning can be used for generative tasks.

---


