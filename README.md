# Cat-Image-Dector-with-1-hidden-Layer
If you are a Deep Learning enthusiast than you must know how important is it to make a cat image classifier in deep learning.
During my course on **Coursera** i have built a strong foundation of neural networks and after completing the course it's time to check how clear are my understnadings.
The basic Structure and process of Project is described below moreover it is an open source project everyone is welcomed come to contribute to it.

**_Structure:_**

  The basic structure of project is that this model is made up of two _2-Layers_ and it is a _Binary-Classifier_ means there is only two classes for which if Y=0 than it is not a cat if Y=1 it is a cat.
        As this model has 2-layers the hidden layer is only one and is made up of _5-Neurons_ the number of neurons in Binary classifier are mostly taken to be one which makes the moidel processing easy.The model structure is as:

  ![image](https://github.com/SARMAD-ALI-cyber/Cat-Image-Dector-with-1-hidden-Layer/assets/113132683/cb21f031-ce4a-4d9b-8fae-427a89491a2f)

        
  We have used _Rectified Linear Unit_ activation function in the hidden layer and _Sigmoid_ activation function in the 2nd layer.For _Relu_ function we have made a function that returns returns Zero when get any negative value and rerturn the value back if get any positive value.To calculate the derivative of Relu function for back-propagation we also have made a Relu_derivative function.It returns x if x is greater than or equal to zero, and returns 0 if x is less than zero.

![image](https://github.com/SARMAD-ALI-cyber/Cat-Image-Dector-with-1-hidden-Layer/assets/113132683/f8463554-98fe-4ca9-9857-24a4c900d9b8)

**_Process:_**

  This project is totaly divided into 4 steps.Let's break through each step and get more details.

**_Step-1:_**

  In the first step we have loaded a data from to files which are .h5 files named as _train_catvnoncat.h5_ for test file it is _test_catvnoncat.h5_  and the source of the files is **Kaggel website a Data-Science company.**After loading our data set we will process the data to make it easier for our model.First we will check the shapes of our data set.The shapes are as follows


![image](https://github.com/SARMAD-ALI-cyber/Cat-Image-Dector-with-1-hidden-Layer/assets/113132683/45e2ea32-4dce-42f0-8ac7-014578056ece)

In most of the deep learning models it is better to flatten  the data set which makes learning easier for our model orignaly the data set is in shape (num_images,height,width,channel). Here the channel is 3 means RGB ranging from 0 to 255. we will also make our channel to 1 so that we only have black and white pixels.Which makes learning faster.

we will acomplish the flatting by this (height x width x channel) so shapes after flattening is.

![image](https://github.com/SARMAD-ALI-cyber/Cat-Image-Dector-with-1-hidden-Layer/assets/113132683/747ea57d-2784-42cd-bfc4-bd2e2f700d60)


To change the channel we divide the data set by 255 so our channel is 1 instead of 3.

![image](https://github.com/SARMAD-ALI-cyber/Cat-Image-Dector-with-1-hidden-Layer/assets/113132683/5dd4f52e-b98e-446d-b4cb-8c61ba857177)


**_Step-2:_**
In the second step we will intialize our parameters.WE will initialize the weights of all layers with small random values and bias with zeros the reason for all this is explained in a  note written by me below:

![image](https://github.com/SARMAD-ALI-cyber/Cat-Image-Dector-with-1-hidden-Layer/assets/113132683/26efb190-3ef6-4fd4-ac8d-e4dfb1c52214)

**_Step-3:_**

In the third step we will propagate through the layers both forward and backward and compute the cost entropy loss with the following formula.

![image](https://github.com/SARMAD-ALI-cyber/Cat-Image-Dector-with-1-hidden-Layer/assets/113132683/50500b51-5422-464f-82bd-9448ec0d3e03)

The formulas of gradient descent we have used for back propagation are listed below:

![image](https://github.com/SARMAD-ALI-cyber/Cat-Image-Dector-with-1-hidden-Layer/assets/113132683/9a9834f1-1356-40eb-832c-628e930b58d2)

The forward propagation is as follows but the function at first layer is Relu:

![image](https://github.com/SARMAD-ALI-cyber/Cat-Image-Dector-with-1-hidden-Layer/assets/113132683/28b299f4-59c8-458a-8288-d649a0b4003a)

**_Step-4:_**

In the last step we will made a function called train model to call all our functions in order which we have made earlier.
The overview is like this:




https://github.com/SARMAD-ALI-cyber/Cat-Image-Dector-with-1-hidden-Layer/assets/113132683/d9c2e74a-3ce1-4504-8dda-35b43a3ca8e8

**_NOTE!_**
This project is an open source project and everyone is welcomed to make it more better it predicts some of the pictures wrong but overall the model has great accuracy.
