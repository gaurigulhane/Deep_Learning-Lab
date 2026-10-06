 Deep Learning & Its Applications Lab

Welcome to the *Deep Learning & Its Applications Lab* repository! This repository contains a curated collection of deep learning experiments, implementation scripts, and reference documentation completed as part of the curriculum.

## 📌 Repository Overview
- **Author:** Gauri Gulhane (Roll No: 23070521054)
- **Topic:** Deep Learning Foundations, Architectures, and Generative Modeling
- **Environment:** Jupyter Notebooks / Google Colab

---

## 📂 Repository Structure

```bash
├── README.md                                             # Project documentation
├── Deep Learning and Its Applications Lab_Experiment_List.pdf  # Lab experiment curriculum
└── Deep_Learning_Lab.ipynb                                # Main notebook containing implementations
```

---

## 🛠️ Experiments & Key Implementations

### 1. Generative Adversarial Networks (GANs) on MNIST
- **Goal:** Train a generative framework to synthesize new, realistic-looking handwritten digits from the MNIST dataset.
- **Architecture details:**
  - **Generator:** Uses fully connected dense layers with `ReLU` activation and a final `Tanh` activation function mapped to standard normalized dimensions ($28 \times 28$ pixels).
  - **Discriminator:** Binary classifier network classifying real vs. synthetic images using `Sigmoid` activation.
- **Optimization Strategy:** Uses dual `Adam` optimizers with learning rates of $0.0002$ and optimized gradient propagation via `@tf.function` compiled training steps for fast execution.

---

## 🚀 How to Run the Code

### Prerequisites
Make sure you have Python 3 installed along with the required libraries:
```bash
pip install numpy tensorflow matplotlib
```

### Running the Jupyter Notebook
1. Clone this repository:
   ```bash
   git clone https://github.com/gaurigulhane/Deep_Learning-Lab.git
   cd Deep_Learning-Lab
   ```
2. Open and run the code in Jupyter Notebook or Google Colab.
