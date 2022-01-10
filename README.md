# Building a CNN
This repository is to illustrate how to construct a simple cnn using Tensorflow with help of jupyter notebook with detailed illustration

## What is a CNN?
CNN stands for Convolutional Neural Network. As the name goes, this Neural Network does convolution on the input images (remember images are nothing but matrix). 

### What is Convolution
It would be easy to remember convolution as wrong matrix multiplication and addition rather than getting into the mathematical formulation for the beginner level. Now let's see what is wrong matrix multiplication and addition in the below figure

![Convolution](https://github.com/VigneshKathirkamar/building_cnn/blob/main/convolution.png)

If you observe the above figure, you can find that our image (a matrix) is getting multiplied by kernel (another matrix) pixel-wise, so that we get 9 pixel values. Then we add all those 9 pixel values and make it one value at the end. Don't forget that we passed a image size of 3x3 (3 rows and 3 colums) and after convolution with a 3x3 kernel, our final product was only one value, i.e 97, which means 9 pixel values at the end of convolution is changed to 1 pixel value. Hope you got the context of convolution from the above figure, and the only new term would be __*kernel*__. Let's get it cleared too.

__Kernel__: Kernel which are also sometimes called as filters are matrices, that move over the images to extract the features of the images. Visit this [site](https://setosa.io/ev/image-kernels/?from=hackcv&hmsr=hackcv.com&utm_medium=hackcv.com&utm_source=hackcv.com) for having a visual understanding of how kernels work

__Stride__: Stride is a unit with which we move the kernel over an image, consider the below image, in which the stride value is 'two' since we move the filter each time by two (pixel) units. Also note that horizonatl sliding and vertical sliding can differ, but it is common to maintain same values for both.

![stride](https://github.com/VigneshKathirkamar/building_cnn/blob/main/stride.gif)

__Pooling__: Pooling is the process of selecting/filtering certain pixel after a convolution. It is used to reduce the dimensions of the feature maps, therby reducing the number of parameters to learn and the amount of computation performed in the network. Find the below image for a better understanding in which max pool is done with filter size of 2x2 and stride 2 in both vertical and horizontal direction.
![pooling](https://github.com/VigneshKathirkamar/building_cnn/blob/main/pooling.png)

Now, we would have seen that after applying convolution and pooling our original image dimension changes, to know what will be the dimension of the processed image after convolution and pooling we have a well established formula to find it as shown below

![formula](https://github.com/VigneshKathirkamar/building_cnn/blob/main/formula.png)

The above formula is pretty intutive, where 
* W -> Width of our Input 
* H -> Height of our Input 
* Fw,Fh -> Width and height of our filter respectively
* Sw,Sh -> Stride units in horizontal and vertical direction respectively  
* P -> Padding

__Note__: Padding in tensorflow has two verbal values instead of numerals, they are "SAME" and "VALID". If padding is set to "SAME" then the input and output shape will be preserved when the stride is 1, If padding is set to "VALID", then the output shape is less than or equal to the input shape. Find the gif attached below for better clarity)

![padding](https://github.com/VigneshKathirkamar/Building_CNN/blob/main/padding.gif)

The one on the left is having padding value as "VALID" and the one on the right is having the padding value as "SAME"






[ref: https://towardsdatascience.com/applied-deep-learning-part-4-convolutional-neural-networks-584bc134c1e2
https://www.geeksforgeeks.org/cnn-introduction-to-pooling-layer/,
https://cs231n.github.io/convolutional-networks/,
https://d2l.ai/chapter_convolutional-neural-networks/padding-and-strides.html]
