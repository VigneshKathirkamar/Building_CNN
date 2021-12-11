# Building a CNN
This repository is to illustrate how to construct a simple cnn using Tensorflow with help of jupyter notebook with detailed illustration

## What is a CNN?
CNN stands for Convolutional Neural Network. As the name goes, this Neural Network does convolution on the input images (remember images are nothing but matrix). 

### What is Convolution
It would be easy to remember convolution as wrong matrix multiplication and addition rather than getting into the mathematical formulation for the beginner level. Now let's see what is wrong matrix multiplication and addition in the below figure

![Convolution](https://github.com/VigneshKathirkamar/building_cnn/blob/main/convolution.png)

If you observe the above figure, you can find that our image (a matrix) is getting multiplied by kernel (another matrix) pixel-wise, so that we get 9 pixel values. Then we add all those 9 pixel values and make it one value at the end. Don't forget that we passed a image size of 3x3 (3 rows and 3 colums) and after convolution with a 3x3 kernel, our final product was only one value, i.e 97, which means 9 pixel values at the end of convolution is changed to 1 pixel value. Hope you got the context of convolution from the above figure, and the only new term would be __*kernel*__. Let's get it cleared too.

__kernel__: Kernel which are also sometimes called as filters are matrices, that move over the images to extract the features of the images. Visit this [site](https://setosa.io/ev/image-kernels/?from=hackcv&hmsr=hackcv.com&utm_medium=hackcv.com&utm_source=hackcv.com) for having a visual understanding of how kernels work

__Stride__: Stride is a unit with which we move the kernel over an image, consider the below image, in which the stride value is 'two' since we move the filter each time by two (pixel) units
![stride](https://github.com/VigneshKathirkamar/building_cnn/blob/main/stride.gif)
