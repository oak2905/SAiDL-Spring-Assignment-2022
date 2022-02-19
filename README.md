# SAiDL-Spring-Assignment-2022
In this assignment I have attempted the question 3C of the SAiDL spring assignment. 

### Choosing the data
While training the model with the complete dataset Oxford IIIT pet dataset, the RAM usage was being exceeded hence only 3 pet classes namely Abyssinian, American bulldog, American Pitbull Terrier have been used in the training, validation, testing dataset.

### Description

1) Preparing the dataset.
    a) Training data - Cropped patches of training images.
    b) Testing and Validation data - Random cropped patches of testing and validation images.
    
2) Building the model
    * Used TensorFlow/Keras to build the SRCNN model.
    * The model used was the classic 9-1-5 model as described in the paper 	[[1501.00092] Image Super-Resolution Using Deep Convolutional Networks](https://arxiv.org/abs/1501.00092) i.e. conv layer 1 has filter sizes 9X9, conv layer 2 has filter sizes 1X1, and conv layer 3 has filter sizes 5X5.
    
3) Training the model with batch size = 64, 20 epochs and loss function being Adam. 

4) Plotting the metrics (loss, accuracy) against the epochs.
    * As we see the plots, the loss function reduces and accuracy improves significantly over the epochs.

5) Predicting the super resolution image of a distorted version of an original image
    * Comparing the PSNR scores of Predicted with original image and distorted with original image proves the point that SRCNN improves super resolution of images.
