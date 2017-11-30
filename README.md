## Project:German Traffic sign Classifier

Overview In this project I have implment a convolutional neural network based traffic sign classifier. I have used mainly LeNet Atchitecture from Yann LeCun's original publication.

This project compromizes of the following steps:

Load the data set (see below for links to the project data set)
Explore, summarize and visualize the data set
Design, train and test a model architecture
Use the model to make predictions on new images
Analyze the softmax probabilities of the new images
The following are the image references from the 43 different German Traffic signs available in the data set used to train test and validate the algorithm.

![alt tag](https://github.com/raghu467/Traffic_sign_classfier/blob/master/Readme_images/43_data_samples.png)

The size of the data-set used for the algorithm are as follows:
![alt tag](https://github.com/raghu467/Traffic_sign_classfier/blob/master/Readme_images/data_details.PNG)

## Data Distrubution histogram for the train, Test and validation data sets:

![alt tag](https://github.com/raghu467/Traffic_sign_classfier/blob/master/Readme_images/train_hist_un_normal.png)
![alt tag](https://github.com/raghu467/Traffic_sign_classfier/blob/master/Readme_images/test_histo_unnormal.png)
![alt tag](https://github.com/raghu467/Traffic_sign_classfier/blob/master/Readme_images/valid_histo_un_normal.png)


From the above histograms we can say that few signs have very less samples in the data set: I have created new data samples by rotating and spatial transformation of the images: The new data distribution can be seen bellow:
![alt tag](https://github.com/raghu467/Traffic_sign_classfier/blob/master/Readme_images/train_hist_normal.png)

Now that we have properly distributred data set to train the algorithm we now convert the image from RGB to GRAY and later nromalize the data set. The data set is converted form RGB to gray scale since it helps to safely reduce the size and also speed-up the training algorithm.

The final model used for trianing is based on LeNet atchitecture it consist which  with the following  are the parameters of the model:

mu = 0
sigma = 0.1
EPOCHS = 10
BATCH_SIZE = 150
Learning rate = 0.005

### Layer 1: Convolutional.
Input = 32x32x1. 
Output = 28x28x6. 
Activation:Relu
Pooling. Input = 28x28x6. Output = 14x14x6.

### Layer 2: Convolutional.
Output = 10x10x16. 
Activation:Relu
Pooling. Input = 10x10x16. Output = 5x5x16.

### Layer 3: Fully Connected. 
Input = 400.
Output = 120.
Activation:Relu

### Layer 4: Fully Connected.
Input = 120.
Output = 84. 
Activation:Relu

### Layer 5: Fully Connected.
Input = 84. 
Output = 43. 
Activation:Relu


The final model accuracy are as follows:
Validation Accuracy = 0.969
Test Accuracy: 0.9230408072471619

I have used the Lenet athitecture  and modified it to meet the requirements of the current problem statement and tweaked the above mentioned parameters to get the accuracy greater than 0.93.

The following are the 5 images take from the internet to test the algorithm.

![alt tag](https://github.com/raghu467/Traffic_sign_classfier/blob/master/Readme_images/data_samples_5.png)

The prediction for the above mentioned 5 images are are follows:

![alt tag] (https://github.com/raghu467/Traffic_sign_classfier/blob/master/Readme_images/web_image_prediciton.png)

The prediction accuracy for the web images is 0.06

If the images would have been better cropped and if the border pixels would have been removed during the prediction could have been imrpoved.Still the speed sign was detected as a speed sign but the number was mis-matched.




 
