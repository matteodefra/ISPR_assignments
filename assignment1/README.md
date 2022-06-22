# Midterm 1

Midterm 1 consisted in the development of a __ARMA__ model for fitting and prediciting the "Appliances" of the avalaible timeseries [Energy Data](https://archive.ics.uci.edu/ml/datasets/Appliances+energy+prediction#).

The mentioned 1D timeseries was first analyzed under a stationary setting and a nonstationary setting.

Experiments were conducted in the following way:
- Each phase consists in a fitting of the time series on a portion of data, fixed at 66% for fitting and 33% for testing;
- At each step, the model is fitted on the training data and the resulting __ARMA__ is used to predict the successive value, and the error is computed;
- At next iteration, the true value of the previous prediction is added to the training data and the model is fitted again, by using the new training data and predicting on the successive one;

Different error threshold were chosen in order to measure the prediction error and, in this way, avoid fitting again the model. In particular the thresholds are $0, 20, 50, 100$.
For each of the error threasholds, different model's order for the $P$ and $Q$ parameter were used, hence the different __ARMA(P,Q)__ are:
```
(2,0),(3,0),(5,0),(2,1)
```

where $P$ is the order of the autoregressor model and $Q$ is the order of the moving average model.
