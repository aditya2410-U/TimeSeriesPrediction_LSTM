# TimeSeriesPrediction_LSTM
The code performs time series forecasting using an LSTM (Long Short-Term Memory) neural network model to predict future values of a monthly milk production dataset. The process involves the following steps:

Data Loading and Visualization: The code loads a dataset of monthly milk production, visualizes the initial data using a line plot, and then decomposes the data to understand any underlying seasonality patterns.

Data Preprocessing: The dataset is split into training and test sets. MinMaxScaler is applied to normalize the data within a range of [0, 1] for better training convergence.

Time Series Generator: The TimeseriesGenerator from Keras is used to create input-output pairs for training the LSTM model. It takes a window of past values as input and predicts the next value.

Model Building and Training: An LSTM neural network model is constructed using Keras Sequential API. The model consists of an LSTM layer followed by a dense output layer. It's trained using the training data with the Mean Squared Error (MSE) loss function and the Adam optimizer.

Loss Visualization: The loss history during training is plotted to assess the training progress.

Generating Predictions: The trained model is used to generate predictions on the test data. A loop is used to iteratively predict each future value using the previous predictions.

Data Transformation: The predicted values are transformed back to the original scale using inverse scaling to make them interpretable.

Visualization of Results: The actual test data and the predicted values are plotted together for comparison.
