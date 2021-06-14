# U-Net-Implementation

This notebook consists of an implementation of U-Net using the following resources:
* **Algorithm**: Ronneberger et al., [U-Net](https://arxiv.org/abs/1505.04597) Convolutional Networks for Biomedical Image Segmentation
* **Dataset**: [The Oxford-IIIT Pet Dataset](https://www.kaggle.com/tanlikesmath/the-oxfordiiit-pet-dataset) (published by Kaggle)
* **Packages Used**: TensorFlow, NumPy, scikit-learn, python-Pillow, imageio, matplotlib

### Before We Code...
**Some Additional Context**: Convolutional Neural Networks have allowed ML enthusiasts to innovate on applications which were once considered computational torment. Today, the innovation of ConvNets are a part of our lives via various applications like Medical Image Computing, Self-Driving Cars, and so on. The popular applications usually use ConvNets for the following purposes -
* Image Classification: Identifying if an image has an item(s) or not
* Object Localization: Locating the classified item in the image
* Object Detection (using Bounding Box): Detecting location of multiple objects in a picture along with their classes
* Image Segmentation: Detecting objects by predicting a label for each pixel in the image
<div align='center'>
<img src="/images/ConvNets.jpeg" alt="Figure 1" width="500" height="350"/>
<caption> <br><u><b>Figure 1</u></b>: Applications of ConvNets <br><i>(source: Detection and Segmentation through ConvNets, towards data science, Medium)</i> <br> </caption>
</div>

### ... And what is U-Net?
U-Net is one of the most popular architectures for Image Segmentation. It was introduced by Olaf Ronneberger, Philipp Fischer, Thomas Brox in 2015 for tumor detection but since has been found to be useful across multiple industries.
<br>
<div align='center'>
<img src="/images/Self-Driving-Car.jpeg" alt="Figure 2" width="400" height="200"/>
<caption> <br><u><b>Figure 2</u></b>: Here's how a self-driving car sees the world through Image Segmentation <br><i>(source: Intro to Artificial Intelligence, Medium)</i> <br> </caption>
</div>

### What's so different about U-Net? 

To allocate a class to each pixel in an image, Image Segmentation requires the downscaled image (due to convolution) to be upscaled to a size closer to the original image. Architectures before U-Net used Dense Layers to upscale images which made them computationally expensive. They also suffered from information loss due to traversal of images across multiple layers. U-Net solves for this by -
* **Upscales images** back to original input size using **transposed convolutions**
* **Retains spatial information** which usually would get lost in multiple ConvNets by using **skip connections**
</font>

<div align='center'>
<img src="/images/u-net-architecture.png" alt="Figure 3" width="600" height="400"/>
<caption> <br><u><b>Figure 3</u></b>: U-Net gets its name from its 'U'-like shape <br><i>(source: https://lmb.informatik.uni-freiburg.de/people/ronneber/u-net/)</i> <br> </caption>
</div>
<br>
