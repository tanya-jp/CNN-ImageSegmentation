# CNN-ImageSegmentation
This project contains two parts and each of them is a `CNN` implemented with `pytorch`.

## First Part
This part is just an exercise to learn better about CNNs and their performance.

## Second Part
The aim of this part is `image segmentation`.
### Data
Since data has a key role in training and testing a `neural network`, a good dataset is vital to have a valuable result. For this purpose, we decided to use data from [CamVid](https://github.com/alexgkendall/SegNet-Tutorial/tree/master/CamVid) part of [SegNet-Tutorial](https://github.com/alexgkendall/SegNet-Tutorial), using:
```
!git clone https://github.com/alexgkendall/SegNet-Tutorial.git
```
- The images and their labels need to get mirrored:
![image](https://user-images.githubusercontent.com/72709191/195537977-5a81fa9d-dabe-46f9-a8e8-0942bddf7c9f.png)

### Neural Network
For image segmentation `U-Net` is used, based on [Convolutional Networks for Biomedical Image Segmentation](https://arxiv.org/pdf/1505.04597.pdf). The netwoork first uses `convolutional layers` and `up-sampling` to extract the properties of images, which are related to the image context. Then, by putting extracted properties and feature map from each step together, local information and context information get combined.
