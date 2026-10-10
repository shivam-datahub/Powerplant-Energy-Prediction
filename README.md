# Powerplant-Energy-Prediction
This repository implements an Artificial Neural Network (ANN) built with PyTorch to predict the net hourly electrical energy output (`PE`) of a Combined Cycle Power Plant using environmental input variables.


# ⚡ Power Plant Energy Prediction using PyTorch (ANN)

This project uses an **Artificial Neural Network (ANN)** built with **PyTorch** to predict the net hourly electrical energy output (`PE`) of a Combined Cycle Power Plant[cite: 2].

---

## 📌 Overview

A Combined Cycle Power Plant uses gas and steam turbines to produce electricity. This model takes 4 environmental variables as input and accurately predicts the power output (`PE`)[cite: 2].

### 📊 Dataset Details
The dataset contains 9,568 rows with the following features[cite: 2]:
* **`AT`**: Ambient Temperature (°C)[cite: 2]
* **`V`**: Exhaust Vacuum (cm Hg)[cite: 2]
* **`AP`**: Ambient Pressure (mbar)[cite: 2]
* **`RH`**: Relative Humidity (%)[cite: 2]
* **`PE`** *(Target Variable)*: Net hourly electrical energy output (MW)[cite: 2]

---

## 🧠 Neural Network Architecture

The regression model is built using PyTorch (`nn.Sequential`)[cite: 2]:
* **Input Layer**: 4 input features (`AT`, `V`, `AP`, `RH`)[cite: 2]
* **Hidden Layer 1**: Linear(4, 6) + ReLU activation[cite: 2]
* **Hidden Layer 2**: Linear(6, 6) + ReLU activation[cite: 2]
* **Output Layer**: Linear(6, 1)[cite: 2]

---

## 📈 Model Performance

* **Optimizer**: Adam[cite: 2]
* **Loss Function**: Mean Squared Error (MSE)[cite: 2]
* **Epochs**: 100[cite: 2]
* **Batch Size**: 32[cite: 2]
* **Training MSE**: ~20.66[cite: 2]
* **Testing MSE**: ~18.89[cite: 2]
* **R² Score**: ~0.934 (93.4% accuracy)[cite: 2]

---

## 📁 Repository Structure

```text
├── ANN_Regression.ipynb    # Jupyter Notebook with full code & training
├── best_model.pt           # Saved PyTorch trained weights
├── powerplant_data.csv     # Dataset file
└── README.md               # Project documentation
