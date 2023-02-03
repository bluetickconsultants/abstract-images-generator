
<h1> Generating Abstract images using Neural Networks </h1>

For generating random colored images we will develop an ANN architecture that takes each pixel value as an input. All inputs are modified by weight and summed. For handling the n-dimensional data as an input we can use the techniques mentioned below.

<br> 

<h3> Techniques used </h3>

<br>

           1 . Numpy
           2 . Statistics 
           3 . Activation functions 
           4 . OpenCV

Selecting the size of an image as an input in the form of height and weight ex: image width = 216 and image height = 216 which gives us a black image.

<img src="/Neural Networks for Abstract Art/images/download.png" width="700" height="400">

<br>
<h1> Neural Network Architecture </h1>
<br>
For creating a Neural Network we need to define input data, Hidden layers, and the number of neurons per layer, and the Activation Function.
Suppose we have (512,512) images. what neural network does is will collect every pixel value fun{i,j} to computer r,g,b,a values.
So total we are having 5 input dimension data. Each pixel converts into 5 different values to generate r,g,b, a, and bias values.
Value = min(image height and image width)
Input1 = i / value - 0.5
Input2 = j / value - 0.5
Z = sqt(input1 + input2)
Z1 = random value from -1 to 1 Alpha 
Z2 = random value from -1 to 1 Bias 

These input values were added with some random weights along with the activation function for each neuron. On selecting the color mode the values get changes for the output layer.

<img src="/Neural Networks for Abstract Art/images/ann.png" width="700" height="400">
<br>

<h1> Activation Functions used </h1>
<br>

             1 . sigmoid
             2 . relu 
             3 . Softmax
             4 . Tanh 

<br>

<h1> Selecting Color Mode </h1>

<br>

The output layers depend on which color mode we select. Using RGB, CMYK, and HSV, and HSL we generated our images. If we are not using any color mode just the input data were gone through a neural network and gives 3 output layers for R, G, B channels. But if we use color mode each pixel again goes under their own maths calculation for changing the values.

Some images generated with RGB color mode

<img src="/Neural Networks for Abstract Art/images/11.png" width="700" height="400">


Some images generated with HSV and HSL color Mode

<img src="/Neural Networks for Abstract Art/images/12.png" width="700" height="400">

Some images were generated using CMYK color mode

<img src="/Neural Networks for Abstract Art/images/21.png" width="700" height="400">


