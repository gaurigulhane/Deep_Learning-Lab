# Deep Learning & Its Applications Lab

Welcome to the official repository for the **Deep Learning & Its Applications Lab**!

This repository serves as a comprehensive portfolio containing all laboratory experiment implementations, datasets, architectures, and theoretical foundations completed during the course.

## 📌 Repository Overview
- **Author:** Gauri Gulhane (Roll No: 23070521054)
- **Curriculum:** Deep Learning & Its Applications Lab
- **Environment:** Google Colab, Jupyter Notebook, TensorFlow, Keras, PyTorch, Python 3

---

## 📂 Complete Laboratory Experiment List

Below is the complete curriculum mapping of experiments designed to build and evaluate deep learning concepts from scratch to generative modeling:

### 🏫 Part 1: Foundations & Classical Neural Networks
* **Experiment 1: Introduction to TensorFlow and PyTorch Frameworks**
  * Understanding tensors, computations, GPU acceleration, automatic differentiation, and execution graphs.
* **Experiment 2: Single-Layer Perceptron (SLP) Implementation**
  * Building a perceptron from scratch to solve linearly separable logical classification tasks (e.g., AND, OR gates).
* **Experiment 3: Multi-Layer Perceptron (MLP) for Multi-Class Classification**
  * Designing an MLP architecture to classify standard datasets like MNIST or Fashion-MNIST using Feedforward propagation and Backpropagation.
* **Experiment 4: Hyperparameter Tuning and Optimization Techniques**
  * Analyzing the performance of different optimizers (SGD, Adam, RMSprop), weight initialization schemes, activation functions (ReLU, Sigmoid, Tanh), and dropout regularization.

### 🖼️ Part 2: Computer Vision & Convolutional Networks
* **Experiment 5: Convolutional Neural Networks (CNNs) for Image Classification**
  * Implementing a CNN classifier with pooling layers, convolutional layers, and flattening to categorize CIFAR-10 images.
* **Experiment 6: Transfer Learning & Fine-Tuning**
  * Leveraging pre-trained state-of-the-art models (such as ResNet50, VGG16, or MobileNet) for targeted custom image classification datasets.

### 📝 Part 3: Sequence Modeling & Natural Language Processing
* **Experiment 7: Recurrent Neural Networks (RNNs) for Sequence Prediction**
  * Designing simple RNN architectures to perform time-series forecasting or text generation.
* **Experiment 8: Long Short-Term Memory (LSTM) Networks**
  * Implementing LSTMs to overcome vanishing gradients and capture long-range dependencies in Sentiment Analysis tasks.

### 🎨 Part 4: Generative Deep Learning (Currently Implemented)
* **Experiment 9: Generative Adversarial Networks (GANs)**
  * Developing a generator-discriminator framework to synthesize realistic digits from randomly sampled latent noise vectors using the MNIST handwritten digits dataset.

---

## 🛠️ In-Depth Implementation: Generative Adversarial Networks (GANs)

### 🎯 Objective
To construct and train a Deep Generative Adversarial Network capable of generating convincing $28\times 28$ pixel images of digits without human supervision.

### ⚡ Architecture Details
1. **Generator ($G$):**
   * **Input:** Random Gaussian noise vector $z \in \mathbb{R}^{100}$
   * **Hidden Layer:** Dense Layer (128 units) with `ReLU` Activation
   * **Output Layer:** Dense Layer (784 units) with `Tanh` Activation (representing normalized $28\times28$ pixels in the range $[-1, 1]$)

2. **Discriminator ($D$):**
   * **Input:** Flat image tensor $x \in \mathbb{R}^{784}$ (both real dataset images and synthetic generator images)
   * **Hidden Layer:** Dense Layer (128 units) with `ReLU` Activation
   * **Output Layer:** Dense Layer (1 unit) with `Sigmoid` Activation outputting probability $P(\text{Real})$

### ⚙️ Training Process & Acceleration
* **Loss Function:** `BinaryCrossentropy` for minimax objective optimisation.
* **Optimization:** Twin `Adam` Optimizers (Learning Rate: $0.0002$ for both Generator and Discriminator).
* **Compilation Acceleration:** Compiled with `@tf.function` computational graph acceleration for high-throughput tensor evaluations inside the Google Colab training loops.

---

## 🚀 Running the Lab Environment

### 1. Prerequisites
Install dependencies directly on your system or environment:
```bash
pip install numpy tensorflow matplotlib
```

### 2. Execution
Clone this laboratory repository and open the interactive notebook:
```bash
git clone https://github.com/gaurigulhane/Deep_Learning-Lab.git
cd Deep_Learning-Lab
jupyter notebook Deep_Learning_Lab.ipynb
```
