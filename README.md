# Fall Prediction Using Biomedical Sensor Data 🧠📉

This project uses machine learning (specifically a neural network) to predict the likelihood of a fall based on biometric sensor inputs such as SpO2, heart rate variability (HRV), sugar levels, and more.

## 🔍 What it does
- Trains a neural network model to classify 3 classes of fall risk
- Uses early stopping to prevent overfitting
- Visualizes training vs. validation performance

## 🧪 Tech Stack
- Python, Pandas, NumPy
- TensorFlow / Keras
- Matplotlib
- Scikit-learn

## 📁 Files
- `Fall_Prediction_Model.ipynb`: Model training & evaluation (Colab notebook)
- `Fall_Prediction_Model.py`: Python script version
- `cStick_data.xlsx`: Sample dataset

## 🚀 How to Run

### Option 1: Run on Google Colab
1. Upload the dataset to your Colab session
2. Open `Fall_Prediction_Model.ipynb`
3. Run all cells!

### Option 2: Run Locally
1. Clone the repo
2. Install dependencies:
   ```bash
   pip install tensorflow pandas numpy matplotlib scikit-learn
   ```

3. Run the script:

   ```bash
   python Fall_Prediction_Model.py
   ```

## 📊 Sample Output

> Plots for accuracy and loss over epochs will be shown after training.

## ⚠️ Notes

* Make sure the dataset (`cStick_data.xlsx`) is in the same directory when running the script.
* This is a prototype for academic/demonstration purposes.

---

Pull requests welcome. 🔧✨

