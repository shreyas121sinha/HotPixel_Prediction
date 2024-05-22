# **Prediction of the coordinates of the pixel which has a value of 255 in a 50x50 grayscale image where all other pixels have a value 0.**

**Supervised Regression using CNN.**

# Requirements installation instruction:

To run the project, the following dependencies may need to be installed (if not already installed).  
**-TensorFlow  
-NumPy  
-MatplotLib  
-scikit-learn**

The following command can be used:  
**pip install tensorflow numpy matplotlib scikit-learn**

# A Brief Project Overview:  

**(1) Dataset Generation:**  
A synthetic dataset with 50000 training examples has been generated. Considering the fact, that the number of possible positions of the hot pixel can be 2500(50x50), a large dataset with at least 50000 examples becomes necessary.

**(2) Splitting the dataset:**
The dataset has been split into 4:1 ratio, with 40000 images in the training dataset and 10000 images in the testing dataset. It has been done to evaluate the performance of the model on the new data and prevent overfitting.

**(3) Model Compilation:**
The model consists of three convolutional layers with ReLU activation functions, followed by a Flatten layer to reshape the output. A single fully connected layer with ReLU activation is added, and the final layer predicts the x and y coordinates of the hot pixel.

The 'Adam optimizer' with a learning rate of '0.01' has been used for training, and the model has been compiled with 'mean squared error loss'.

<img src= "https://photos.app.goo.gl/zZ1CiYcvVnJBaQ5n8" alt= "Image not found">

**(4) Model Training:**
The number of epochs and the batch size have been set to 10 and 256 respectively for the training of the model, to strike a balance between the model accuracy, the model generalization and the training process time. 

A training accuracy of '98.96%' and a validation accuracy of '99.17%' have been obtained after 10 epochs. Training it for any more number of epochs does not appear necessary since there are no signs of any significant improvements in the accuracies after continuing further.

The proximity in the values of both accuracies indicates that the model has not overfit on the training dataset and that it would perform well on the new data.

**(5) Training Visualization:**
This section displays the training progress of the model through a plot. The plot illustrates the training and the validation accuracies of the model over epochs. This visualization provides insight into the performance and the convergence of the model over time.

**(6) Model Prediction Evaluation:**
In the following section, 10 examples from the validation dataset have been randomly selected and passed to the model. The actual and the predicted coordinates for each case have been printed and compared through visualisation. The 'Blue dot' represents the 'predicted value' and the 'red dot' represents the 'actual values'.

_(The near overlapping of the **blue dot** and the **red dot** in each of the 10 cases showcases that the model has been very accurate in making predictions.)_






```python

```
