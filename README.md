##Project:German Traffic sign Classifier

Overview In this project I have implment a convolutional neural network based traffic sign classifier. I have used mainly LeNet Atchitecture from Yann LeCun's original publication.

This project compromizes of the following steps:

Load the data set (see below for links to the project data set)
Explore, summarize and visualize the data set
Design, train and test a model architecture
Use the model to make predictions on new images
Analyze the softmax probabilities of the new images
The following are the image references from the 43 different German Traffic signs available in the data set used to train test and validate the algorithm.

![alt tag](https://github.com/raghu467/Traffic_sign_classfier/blob/master/Readme_images/43_data_samples.png)

##Data Distrubution histogram for the train, Test and validation data sets:

![alt tag](https://github.com/raghu467/Traffic_sign_classfier/blob/master/Readme_images/train_hist_un_normal.png)
![alt tag](https://github.com/raghu467/Traffic_sign_classfier/blob/master/Readme_images/test_histo_unnormal.png)
![alt tag](https://github.com/raghu467/Traffic_sign_classfier/blob/master/Readme_images/valid_histo_un_normal.png)


From the above histograms we can say that few signs have very less samples in the data set: I have created new data samples by rotating and spatial transformation of the images: The new data distribution can be seen bellow:
![alt tag](https://github.com/raghu467/Traffic_sign_classfier/blob/master/Readme_images/train_hist_normal.png)

Now that we have properly distributred data set to train the algorithm we now convert the image from RGB to GRAY and later nromalize the data set. As mentioned before the CNN model is based on LeNet architecture with the following dimentions in the each Layer: Layer 1: Convolutional. Input = 32x32x1. Output = 28x28x6. Activation:Relu Pooling. Input = 28x28x6. Output = 14x14x6.

Layer 2: Convolutional. Output = 10x10x16. Activation:Relu Pooling. Input = 10x10x16. Output = 5x5x16.

Layer 3: Fully Connected. Input = 400. Output = 120. Activation:Relu

Layer 4: Fully Connected. Input = 120. Output = 84. Activation:Relu

Layer 5: Fully Connected. Input = 84. Output = 43. Activation:Relu

In this project, you will use what you've learned about deep neural net
