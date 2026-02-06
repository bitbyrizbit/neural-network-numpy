# Neural Network From Scratch (NumPy)

This project implements a **shallow neural network from scratch using NumPy** to study **backpropagation behavior, activation functions, and gradient flow**.

The goal is **conceptual understanding**, not library usage or production performance - every forward and backward computation is written explicitly.

---

## Objectives

* Implement a **fully connected neural network from first principles**
* Understand **forward propagation and backpropagation**
* Study **vanishing gradients** in sigmoid networks
* Compare **Sigmoid vs ReLU** activation behavior  
* Analyze the effect of **hidden layer width**
* Visualize **loss curves** and **decision boundaries**

---

## Dataset

The project uses the **make_moons** dataset from `sklearn.datasets`.

**Why make_moons?**

* Non-linearly separable
* Only **2 input features**, ideal for visualization
* Clearly demonstrates why hidden layers are necessary

The dataset is used **only as a data source** - no sklearn models are involved.

---

## Model Architecture

* Input layer: **2 neurons**
* Hidden layer: configurable (experimented with different sizes)
* Output layer: **1 neuron (Sigmoid)**
* Loss function: **Binary Cross-Entropy**
* Optimization: **Full-batch Gradient Descent**

---

## Core Components Implemented

* Weight and bias initialization
* Forward propagation
* Sigmoid and ReLU activations
* Binary cross-entropy loss
* Analytical backpropagation
* Gradient descent parameter updates

All operations are **fully vectorized using NumPy**.

---

## Experiments Conducted

### 1. Activation Function Comparison

* Sigmoid vs ReLU
* Observed convergence speed
* Studied gradient saturation effects

### 2. Effect of Hidden Neurons

* Small hidden layer (low capacity)
* Larger hidden layer (higher capacity)
* Observed changes in decision boundary flexibility

---

## Visualizations

* **Loss vs Epochs** plots
* **Decision boundaries** for both Sigmoid and ReLU networks

These plots make optimization behavior and representational power immediately interpretable.

---

## Key Observations

* Sigmoid activation shows **slower convergence** due to saturation and vanishing gradients
* ReLU preserves gradient flow, enabling **faster and more stable training**
* Increasing hidden neurons improves expressive power but increases model complexity
* Architectural choices directly impact optimization dynamics

---

## Project Structure

```
neural-network-numpy/
│
├── neural_network_from_scratch.ipynb   # Complete implementation & experiments
├── requirements.txt                    # Minimal dependencies
├── .gitignore                          # Git ignore rules
└── README.md                           # Project documentation
```

---

## How to Run

1. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

2. Open the notebook:

   ```bash
   jupyter notebook neural_network_from_scratch.ipynb
   ```

Run all cells sequentially to reproduce experiments and visualizations.

---

## Takeaway

This project demonstrates **how neural networks actually learn**, beyond high-level APIs - highlighting the impact of activation functions, depth, and gradient flow on optimization.
