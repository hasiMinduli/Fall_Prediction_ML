# 🧠 Fall Prediction Model Based on IoMT Framework (Re-implementation)

This repository contains the re-implementation and optimization of a fall prediction model inspired by the research paper:

**"cStick: A Calm Stick for Fall Prediction, Detection, and Control in the IoMT Framework."**

---

## 📚 Abstract

Falls are a leading cause of injuries among the elderly, making their prediction and prevention vital. This project re-implements the model proposed in the **cStick** paper and optimizes it for real-world constraints, such as limited public data. Using physiological and environmental sensor data, we built and enhanced a neural network model to classify fall events into three categories: *No Fall, Fall Prediction, and Fall Detection*.

---

## 🧪 Dataset

- Public subset of original dataset from the paper (2,040 samples)
- Features used:
  - Heart Rate Variability (HRV)
  - Accelerometer Readings
  - Blood Sugar Levels
  - SpO2 (Oxygen Saturation)
  - Grasping Pressure
  - Distance to Nearest Object
- Target Labels:
  - 0: No Fall
  - 1: Fall Prediction
  - 2: Fall Detection

---

## 🛠️ Model Architectures

### 🔹 Original Model:
- Input: 6 features
- 2 hidden layers (20 units each), ReLU activation
- Output: 3 classes (Sigmoid)
- Optimizer: SGD (0.01 LR), Epochs: 200

⚠️ Result: **100% train accuracy** → Overfitting 😬

---

### 🔸 Optimized Model:
- Hidden Layers: 8 + 4 units
- Activation: ReLU
- Output Layer: Sigmoid (3-class)
- Optimizer: **Adam (0.0001 LR)**
- Regularization: L2 (0.05)
- Dropout: 20%
- Early Stopping: Enabled (epoch 34)

✅ Result: **97.06% validation accuracy** with improved generalization!

---

## 📈 Results Overview

| Metric                | Original Model         | Optimized Model         |
|----------------------|------------------------|-------------------------|
| Hidden Layers         | 2 × 20                 | 8 → 4                   |
| Optimizer             | SGD                    | Adam                    |
| Regularization        | None                   | L2 (0.05)               |
| Dropout               | None                   | 20%                     |
| Test Accuracy         | Overfit (100%)         | 97.06%                  |
| Early Stopping        | ❌                     | ✅ Epoch 34             |

---

## 📊 Plots

Training & validation accuracy and loss plots for both original and optimized models are available in the notebook.

---

## 🚀 How to Run

### Option 1: Run on Colab  
[🔗 Open in Colab](#)

1. Upload `cStick_data.xlsx`
2. Run all cells in `Fall_Prediction_Model.ipynb`

### Option 2: Run Locally

```bash
git clone https://github.com/hasiMinduli/Fall_Prediction_ML.git
cd Fall_Prediction_ML
pip install -r requirements.txt  # Or install libraries manually
python Fall_Prediction_Model.py
````

---

## 💡 Insights

* Neural networks **must** be adjusted based on data size and quality
* Regularization + adaptive optimizers like Adam can save you from overfitting hell
* Even a smaller dataset can work if you optimize architecture & training strategy

---

## 🩺 Future Use in IoMT

The optimized model is compact and robust, making it suitable for integration into embedded healthcare systems like **cStick**, supporting real-time elderly fall prevention.

---

## 📄 Report

A full technical write-up of the re-implementation and analysis is available [here](#) *(upload your PDF/report as a GitHub release or markdown if you want)*.

---

## ✨ Credits

Original paper: [cStick: A Calm Stick for Fall Prediction, Detection, and Control in the IoMT Framework](#)
Re-implementation by: **@hasiMinduli**

---

## 🤝 Contributions

Open to feedback and suggestions! Fork the repo and drop a PR or reach out!

📄 **Full Report**: [Download the PDF](./Final_Report.pdf)
