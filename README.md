# Fall Prediction Model 🧠🚨

A neural network built in Google Colab to predict the risk of a fall using biometric and motion data.

## 📊 Dataset

Includes:
- `cStick_data.xlsx`  
  with features:
  - Distance
  - Pressure
  - HRV
  - Sugar level
  - SpO2
  - Accelerometer  
  and the label:
  - Fall (3 classes)

## 🧠 Model

- Built with TensorFlow & Keras
- Uses early stopping at a specific epoch (34)
- Includes dropout and L2 regularization
- Visualizes accuracy/loss per epoch

## 🚀 How to Run

### Option 1: In Google Colab
1. Open `fall_prediction_model.ipynb` in [Google Colab](https://colab.research.google.com/)
2. Upload `cStick_data.xlsx`
3. Run all cells

### Option 2: Locally

```bash
pip install -r requirements.txt
jupyter notebook fall_prediction_model.ipynb
```
🧪 Dependencies
```bash
Copy code
numpy
pandas
scikit-learn
tensorflow
matplotlib
openpyxl
```
⚠️ Make sure you don’t push sensitive medical data publicly if this was collected from real-world sources.

🧑‍💻 Author
Hasi Minduli

🪪 License
MIT License © 2025 Hasi Minduli
