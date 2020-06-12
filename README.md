# Cityscapes semantic segmentation

This code is an implementation of semantic segmentation based on the cityscapes dataset.


## Dataset

Cityscapes images where each image contains the actual image on the left and the masked image on the right. The citysapes data is split into Train and Validation. There are around 3000 training images and 500 validation images. You can download the data from the kaggle page

![cityscapes images in kaggle](https://www.kaggle.com/dansbecker/cityscapes-image-pairs)

Here's a sample image

![sample image](https://github.com/azharul/semantic_segmentation/blob/master/sample_img.jpg)

## Implementation

    1. It is implemented in google colab using GPUs
    2. Implemented using Unet with skip connections (img not mine)
    ![Unet](https://github.com/azharul/semantic_segmentation/blob/master/unet_img.jpg)
    3. Cityscapes has many objects marked. Here, segmentation of streets were done only.

## Operations

Four operations:
  1. conv2d_down: Regular convolutions with activation
  2. maxpool_down: Maxpooling with padding
  3. conv2d_up: Transposed convolution for upsampling
  4. maxpool_up: Upsampling the inputs
  
## Output 
Here is a sample output image and its corresponding mask that the model generats. As we've only focused on streets, only the street is masked.

![A sample output image](https://github.com/azharul/semantic_segmentation/blob/master/output.png)
