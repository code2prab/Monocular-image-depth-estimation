# Monocular-image-depth-estimation
The NYU-Depth V2 data set is comprised of video sequences from a variety of indoor scenes as recorded by both the RGB and Depth cameras from the Microsoft Kinect. It features:
  -->1449 densely labeled pairs of aligned RGB and depth images
  -->464 new scenes taken from 3 cities
  -->407,024 new unlabeled frames
Dataset used can be downloaded from this link: https://cs.nyu.edu/~silberman/datasets/nyu_depth_v2.html

- We use the NYU Depth V2 Dataset for training and testing. The RGB image and the depth image in the dataset are both of size 640x480. During training, the RGB image is loaded as 640x480 and the depth image is loaded and then resized to 160x120. The input of the network is a RGB image with size 640x480, and the output is a grayscale image of size 160x120, which is the depth map we need.

- Started with selecting model as Feature Pyramid Network (FPN) with ResNet101 as backbone.
- FPN is an effective backbone for monocular depth estimation because of its ability to extract features and semantics at different scales. It can achieve its potential if guided by proper loss functions.
- Two consecutive 3x3 convolutions for feature processing.
- ReLU is used as activation function in the last two convolutional layers. No non-linearity in the top-down branch of FPN.
- Outputs prediction of size ¼.
- Learning rate decay is deployed during training.

## ARCHITECTURE:
![image](https://user-images.githubusercontent.com/100025529/193354334-7f2820a7-a199-42cc-b1b6-c94e3e5b7851.png)

