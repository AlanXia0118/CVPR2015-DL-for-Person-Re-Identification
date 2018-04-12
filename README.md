# CVPR2015-DL-for-Person-Re-Identification
Implementation of Deep Learning Architecture for Person Re-Identification, in CVPR2015.

# Enviroment
Packages utilized in this project including:  
* python 3.5.4  
* opencv 3.1.0  
* matplotlib 2.0.2  
* numpy 1.12.1
* keras 2.1.5

# Dataset
The current model was trained on CUHK01 dataset which consists of 971 identities, with 2 images per person in each view. You can check for more details on http://www.ee.cuhk.edu.hk/~xgwang/CUHK_identification.html.<br>
More specifically, we take as input cropped and augmented pictures instead of raw photos, which we will discuss later in training process.

# Overall Architecture
As represented explicitly in the paper, the model is composed of tied convolution layers and higher layers that compute relationships between two pictures, sharing similar attributes with Siamese neural networks.<br>
You can probably gain more intution by referring to related work.
<br>
<br>
![](https://github.com/AlanXia0118/Resource/blob/master/DL-for-ReID/model.png)
<br>
<br>

# Visualized prediction
`predict_visualization.py` is prepared for predicting on your own pairs of identities, employing opencv and matplotlib packages to realize the visualization. You can change the paths to be your model and image at the start of the script:

```
# predict on your own pairs of identities
img_path1 = './test_dataset/9_1.png'
img_path2 = './test_dataset/8_1.png'
```
A pre-trained model was kept for you in `~/model`. Since we trained the model using normalized data, mean images of dataset are necessary for predicting. Accordingly, one mean images for each channel is provided in `~/mean_img`. 


