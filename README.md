# This Project is based on Autoencoder and XAI to find IoT network Attack certainty
Our approach involves an Explainable AI framework combined with Deep Autoencoders to enhance security in IoT networks against attacks. 
An autoencoder model's reconstruction error is harnessed to identify anomalies within the IoT network, termed as Anomaly Score. 
These anomalies are instances with notably high reconstruction error values.
To establish a benchmark, we determine a threshold for the reconstruction error using a benign training dataset. 
When an incoming data point showcases an anomaly, our explanatory model should elucidate why the autoencoder struggled to predict (reconstruct) that particular instance effectively.
Connecting error to explanation, our method computes the SHAP (Shapley) values of the output features and contrasts them with the actual anomalous values of the input.
Subsequently, the features in the error list are arranged in descending order. 
Our objective is to identify the top R features, which form a set of selected features.
Utilizing SHAP values, our model offers insights into the features that led to high reconstruction errors within the top R features. 
By dissecting feature influence and leveraging domain expertise, we confidently differentiate whether the detected anomaly signifies an attack or a typical anomalous behavior in the network. 
For experimental purposes, we employed the USBIDS dataset
