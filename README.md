<h1 align="center"> Generating Abstract images using Neural Networks</h1>

<hr>

<div align="center">
  <img src="https://user-images.githubusercontent.com/88481845/216519984-25edbc6e-b31e-4d9b-9993-5dd4ff0be772.jpg">
</div>

<hr>

Artificial neural networks are comprised of node layers containing an input layer, one or more hidden layers, and an output layer. Each node connects to another and has an associated weight and threshold value.

For generating random colored images we will develop an ANN architecture that takes each pixel value as an input. All inputs are modified by weight and summed. For handling the n-dimensional data as an input we can use the techniques mentioned below.

<br> 

<h3> Techniques used </h3>

<br>

           1 . Numpy
           2 . Statistics 
           3 . Activation functions 
           4 . OpenCV

Selecting the size of an image as an input in the form of height and weight ex: image width = 216 and image height = 216 which gives us a black image.

<img src="https://user-images.githubusercontent.com/88481845/216520174-3bbb8b58-47d7-4d1d-bb03-52bb8fcff6ee.png" width="700" height="400">

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


<img src="https://user-images.githubusercontent.com/88481845/216520539-733dea11-7baa-47d3-a359-4de4392ce03b.png" width="700" height="400">
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

## Some images generated with RGB color mode

<table>
  <tbody>
    <tr>
      <td>
        <img src="https://user-images.githubusercontent.com/88481845/216521014-08fb4850-bb0e-49dc-a926-7307882d459e.png">
      </td>
      <td>
      <img src="https://user-images.githubusercontent.com/88481845/216521036-73bfaf0a-3344-4db5-8a3b-4982894b7306.png">
      </td>
    </tr>
  </tbody>
</table>




## Some images generated with HSV and HSL color Mode

<table>
  <tbody>
    <tr>
      <td>
        <img src="https://user-images.githubusercontent.com/88481845/216521475-a6be66ee-74cb-4097-bfa9-8b607b231a53.png" width="350" height="250">
      </td>
      <td>
      <img src="https://user-images.githubusercontent.com/88481845/216521940-c65b9af3-82ee-4789-b1f4-672935bb05ca.png" width="350" height="250">
      </td>
    </tr>
  </tbody>
</table>

### Converting input values into specified color mode

Changing input data into CMYK format by adding their input weights
The R, G, B values are divided by 255 to change the range from 0 to 1.
R = R / 255 , G = G / 255 , B = B / 255
Value k can be calculated from RGB k = 1 - max(R,G,B)
The cyan color will be calculated from red and k[black] c = (1-R-K) / (1-K)
The Magenta color will be calculated from green and black m = (1-G-K) / (1-K)
The yellow color will be calculated from blue and black y = (1-B-K) / (1 - K) 

## Some images were generated using CMYK color mode

<table>
  <tbody>
    <tr>
      <td>
        <img src="https://user-images.githubusercontent.com/88481845/216521683-da2c769e-6100-4740-8000-338995cbfb0e.png">
      </td>
      <td>
      <img src="https://user-images.githubusercontent.com/88481845/216521738-8fd4da53-1806-47a6-873a-55dadeaf9453.png">
      </td>
    </tr>
    <tr>
      <td>
        <img src="https://user-images.githubusercontent.com/88481845/216521804-5e41bc32-8d0f-481b-9c06-4745dbc386af.png">
      </td>
      <td>
      <img src="https://user-images.githubusercontent.com/88481845/216521856-77dfd820-7cd6-4bac-8f15-be3cf8df8048.png">
      </td>
    </tr>
  </tbody>
</table>

## Useful Information

### References
- [Generating Abstract images using Neural Networks](https://www.bluetickconsultants.com/generating-abstract-images-using-neural-networks.html)

## Other Projects

To view all other open source projects visit
  - [ Open Source Projects ](https://www.bluetickconsultants.com/open-source.html) 
  - [ Open Source Repositories ](https://github.com/orgs/bluetickconsultants/repositories)

## Author

[Bluetick Consultants LLP](https://www.bluetickconsultants.com/)
  #### contact us at admin@bluetickconsultants.com

<img src="https://user-images.githubusercontent.com/88481845/215745914-16aa10a5-f24b-4fa9-b1be-432454487788.png" width="50%">
