# Image-Style-Transfer-Pytorch-Implementation

## Description

This is based on the thesis Perceptual losses for real-time style transfer and super-resolution. In European conference on computer vision. I will be transferring the style of vincent van goh's famous painting the stary night into my own images. 
The network architecture is shown below. 

<img src="model.png" height="300"/>

In the image transformation networks, only strided and fractionally strided convolutions are used for downsampling and upsampling without any pool- ing layers. It has five residual blocks, with each conv layers followed by batch normalization and ReLU nonlinearities except for the last layer. All convolutional layers use 3x3 kernels except for the first and last layers which applies 9x9 kernels. 

Perceptual loss functions are defined as the functions that measure high- level perceptual and semantic differences between images. They utilize the loss network phi which are pretrained for image classification. This phi in this experiment is based on the 16-layer VGG network pretrained on the ImageNet dataset. The final loss function is shown below. 

<img src="loss.png" height="50"/>

## Results
Model trained on 'Starry Night' style. 
<p align="center">
    <img src="style/starry-night.jpg" height="200px">
</p>

<p align="center">
    <img src="result/img1.jpg" height="300px">
    <img src="result/fig1.png" height="300px">
</p>

<p align="center">
    <img src="result/img2.jpg" height="300px">
    <img src="result/fig2.png" height="300px">
</p>

<p align="center">
    <img src="result/img3.jpg" height="300px">
    <img src="result/fig3.png" height="300px">
</p>


