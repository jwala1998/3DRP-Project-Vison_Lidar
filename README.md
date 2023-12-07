# 3DRP-Project-Vison_lidar

# Road Detection using Deep Learning

## Abstract

In this work, a deep learning approach is developed and tested to accomplish the crucial task of road detection using RGB and LIDAR point cloud data of the scene. The work consists of several Fully Convolutional Neural Networks (FCNs) which are trained to carry out road detection by using one of the three input types as follows:

1. **RGB Image**: The FCN trained with only RGB image data.
2. **RGB Image with LIDAR Overlay**: The FCN trained with RGB image and LIDAR point cloud heat map overlaid onto the camera view.
3. **Fusion Dataset**: A 3-channel dataset containing the mean of RGB values, intensity of RGB values, and the depth spatial information obtained from the point cloud.

The three FCNs were trained and evaluated on the respective input datasets, achieving an intersection over union accuracy of:

- FCN trained with only RGB image data: **0.82**
- FCN trained with LIDAR point cloud overlaid on RGB image: **0.8123**
- FCN trained with fusion dataset: **0.7954**

## Definitions of Files

1. **`Fusion_cleaned.ipynb`**: Fuse RGBD to LIDAR.
    - This file contains the code for combining RGB and LIDAR data.
    - It outputs three types of data:
      1)Segmented point cloud overlaid on image
        2)Image with 6 channels i.e. X ,Y , Z and RGB
        3)Image with 4 channels.
    - Modify the path files according to the need.
    - Download the data from Kitti road dataset for left camera
    - Comment out/in according to output needed 
    - It outputs three types of data: 
        1)Segmented point cloud overlaid on image
        2)Image with 6 channels i.e. X ,Y , Z and RGB
        3)Image with 4 channels.      

2. **modefied_vgg_model.ipynb`**: Experimental model (doesn't work).
    - This file includes an old VGG architecture and a new base CNN architecture used in the project.
    - This is an attempt to input 6 channel image in the vgg network
  
3. **Final_Road_detection_XYZRGB.ipynb**: Model Training and definition
   - This file contains the code that extracts the important features from RGBXYZ.npy files for each image and uses these data along with ground thruth data to tran a FCN for the application of road segmentation
   - It outputs a mask or a overlay on the RGB image of camera view as per the users choice
   - Modify the path files according to the need.
   - Download the data from Kitti road dataset for left camera
   - Comment out/in according to output needed
     
4. **Road_detection_final_fusion.ipynb**: Model Training and definition
   - This file contains the code imports each image with LIDAR overlay and uses these data along with ground thruth data to tran a FCN for the application of road segmentation
   - It outputs a mask or a overlay on the RGB image of camera view as per the users choice
   - Modify the path files according to the need.
   - Download the data from Kitti road dataset for left camera
   - Comment out/in according to output needed

5. **Road_detection_final_RGB.ipynb**: Model Training and definition
   - This file contains the code that each image and uses these data along with ground thruth data to tran a FCN for the application of road segmentation
   - It outputs a mask or a overlay on the RGB image of camera view as per the users choice
   - Modify the path files according to the need.
   - Download the data from Kitti road dataset for left camera
   - Comment out/in according to output needed 

## Data Representation

- **Image**: The visual representation of the scene captured either in RGB or RGB with LIDAR overlay.
- **Label**: The ground truth data indicating the presence or absence of a road.

## Evaluation Metrics

- **Intersection over Union (IoU)**: A measure of the overlap between the predicted road area and the ground truth.

## Results

Insert any additional details about the results, graphs, or visualizations in this section.

## Table of Contents

- [Abstract](#abstract)
- [Definitions of Files](#definitions-of-files)
- [Data Representation](#data-representation)
- [Evaluation Metrics](#evaluation-metrics)
- [Results](#results)

