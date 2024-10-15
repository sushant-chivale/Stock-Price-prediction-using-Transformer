# Stock-Price-prediction-using-Transformer
This repository contains the code for the project "Forex Stock Price Prediction using Transformers and Time Embeddings". The project utilizes the Transformer-XL architecture and time embeddings to predict Forex stock prices. It is written in TensorFlow 2.9.1.

**Table of Contents:**<br>
About the Project<br>
Dataset Description<br>
Preprocessing<br>
Model Architecture<br>
Evaluation<br>
Conclusion<br>

**About the Project**<br>
The foreign exchange (Forex) market is one of the largest financial markets globally, with an average daily trading volume exceeding $5 trillion. Predicting price movements in such markets is challenging due to their dependency on various factors, including economic events, interest rates, political developments, and global news.<br>

This project explores the use of transformer-based deep neural networks for Forex stock market price prediction. Specifically, we implement the Transformer-XL architecture, which excels at handling long sequences. Additionally, time embeddings are used to encode time-related information in the input data.<br>

Our model has been tested on the EUR/USD Forex pair, and we compared its performance against several baseline models. The model achieved a mean absolute error (MAE) of 0.0004 on the test set, marking a 20% improvement over the best-performing baseline model.<br>

**Dataset Description**<br>
We use the IBM stock price history dataset, covering the period from 1962-02-16 to 2020-01-31. The dataset includes daily values for:

Open: The stock's opening price for the day.<br>
High: The highest price during the trading day.<br>
Low: The lowest price during the trading day.<br>
Close: The stock's closing price for the day.<br>
Volume: The number of shares traded.<br>
The dataset comprises 14,588 entries, providing rich historical data for training the model.

**Preprocessing**<br>
Before training the model, the dataset undergoes the following preprocessing steps:

**Normalization:** The price values are normalized to ensure all features contribute proportionally.
Time Series Transformation: The stock prices are converted into sequences, which the Transformer-XL can efficiently process.
Time Embeddings: To incorporate time-related information, we use time embeddings that encode the temporal position of each data point.

**Model Architecture**
We implement the Transformer-XL architecture, which is designed to handle long-term dependencies in time series data. Its ability to process long sequences using attention mechanisms allows it to excel over traditional models like RNNs and LSTMs.

**Key Features:**<br>
**Self-attention mechanism:** Allows the model to weigh different parts of the input sequence, focusing on the most relevant information.<br>
**Time embeddings:** Capture temporal information, helping the model learn time-dependent patterns in stock prices.

**Evaluation**<br>
The model is evaluated on the EUR/USD Forex pair using the Mean Absolute Error (MAE) as the primary metric. The model outperformed several baseline models, achieving an MAE of 0.0004 on the test set, a significant improvement of 20% over the best baseline.

**Conclusion**<br>
In this project, we demonstrated the effectiveness of transformer-based deep neural networks in predicting Forex stock prices. We compared the performance of Transformer-XL with other models like RNNs and LSTMs, and found that transformers significantly outperform them, thanks to their ability to capture long-range dependencies via attention mechanisms.
