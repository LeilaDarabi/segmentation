# segmentation
segmentation_img
In this repository we aim to apply U-Net for segmentation on a map.	
There are four classes of areas in this map.

1 - reconstructing mask
2 - pre processing for training (due to the limitation of resources such as GPU, we need to split the image (main image and its mask) to small images(patches) with the size of 256*256.
3 - to train the model we use U-Net architecture with 23 convolutional layers. We used Dice loss as loss function and IoU score as metrics.
4 - to train the model we splitted the data to Train, Validation and Test,  we trained model in 100 epoch, with learning rate 0.001.


Reconstruction of the mask for training the model: 
we created a mask image where each pixel corresponds to a specific land cover class. 
Then we assign unique values to each land cover class in the mask.

0 - Background  Class
1 - Heath Class
2 - Grassland Class
3 - Forest Class
4 - Agriculture Class


