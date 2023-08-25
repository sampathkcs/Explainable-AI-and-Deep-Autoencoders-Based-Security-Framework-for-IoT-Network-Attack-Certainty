# This Project is based on Autoencoder and XAI to find IoT network Attack certainty
Explainable AI and Deep Autoencoders-Based Security Framework for IoT Network Attack Certainty
We use the reconstruction error of an autoencoder model to define IoT network anomalies (Anomaly Score)
Anomalies are instances with high reconstruction error values.
A threshold for the reconstruction error is estimated using a benign training dataset 
If an anomaly exists in the incoming data, the explanatory model should be able to explain why this instance could not be well predicted (reconstructed) by the autoencoder model
Error is linked to an explanation and the proposed method calculates the SHAP values of the output features and compares them to the true (anomalous) values of the input
Then the features in the error list need to be reordered in a descending order such that find top R features which includes a set of selected features  
The model uses SHAP values to describe which features were responsible for each of the high reconstruction errors in top R features
Through analyzing feature influence and leveraging domain expertise, we can confidently distinguish whether the anomaly corresponds to an attack or a typical anomalous behavior
