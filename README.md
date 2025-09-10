# 📈 Recurrent Neural Network (RNN) – Stock Price Prediction

This project implements a **Recurrent Neural Network (RNN)** with **LSTM layers** to predict the stock price of Google using historical data.  
The model is trained on the **Google Stock Price Training dataset** and tested on the **Test dataset** (January 2017).

---

## 🛠️ Project Structure

1. **Part 1 – Data Preprocessing**
   - Import training dataset (`Google_Stock_Price_Train.csv`)
   - Feature scaling using `MinMaxScaler`
   - Create time-series sequences (60 timesteps → 1 output)
   - Reshape data for RNN input

2. **Part 2 – Building and Training the RNN**
   - Sequential Keras model
   - Four stacked **LSTM layers** with **Dropout** regularization
   - Output layer with 1 unit (predicted stock price)
   - Compile with **Adam optimizer** and `mean_squared_error` loss
   - Train with 100 epochs, batch size = 32

3. **Part 3 – Making Predictions and Visualization**
   - Import test dataset (`Google_Stock_Price_Test.csv`)
   - Generate input sequences from combined train + test data
   - Predict stock prices using trained RNN
   - Visualize **Real vs Predicted stock prices** with Matplotlib

---

## 📂 Files Required
- `Google_Stock_Price_Train.csv` – Training dataset  
- `Google_Stock_Price_Test.csv` – Testing dataset  
- `rnn_stock_prediction.py` – Python script containing the full code  

---

## ⚙️ Installation

1. Clone the repo or copy the script.
2. Install dependencies:
   ```bash
   pip install numpy pandas matplotlib scikit-learn keras tensorflow

How to run:
python rnn_stock_prediction.py
