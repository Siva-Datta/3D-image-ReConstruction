# Depth Estimation and 3D Image Reconstruction
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/bsivadatta/3D-image-ReConstruction/blob/master/Training.ipynb)


- Predicting the depth of the objects, construct 3D images from 2D images <br/>
- Work is based on [High Quality Monocular Depth Estimation via Transfer Learning](https://arxiv.org/abs/1812.11941)<br/>
by Ibraheem Alhashim and Peter Wonka<br/>

## DEPTH ESTIMATION
**Dataset**<br/>
[NYU V2](https://tinyurl.com/nyu-data-zip)

## Training 
- Run the notebook Training.ipynb after you place the "data" folder of the nyu-dataset from the link given above in the same directory as the notebook file.
- Default model is based on MobileNetV2. To train on different models , replace the content in model.py with the codes given in the models directory.

**Pretrained models** are available at:<br/>

- Models I trained are available [here](https://drive.google.com/drive/folders/1C88ENnOCOi_5eeusYJcFNieDSWYgawCk?usp=sharing) , models have been saved in folders with names in the format "architecturename_shapeofinput_numberofepochs" (full refers to 480x640 input shape)
- Results of each of these models are below.<br/>
- Run the evaluate notebook in evaluate directory using appropriate model and input-size for evaluation.<br/>
- Evaluation was done on the [nyutest_data](https://s3-eu-west-1.amazonaws.com/densedepth/nyu_test.zip) compiled in .npy format.<br/>

- Results obtained <br/>
![results](https://github.com/bsivadatta/3D-image-ReConstruction/blob/master/results/results.jpg)<br/>

**Sample outputs using our MobileNetV2 model on Tensorflow 2.x Have been shown clearly in the Demos Folder**


## 3D Reconstruction from rgb and depth
- Run either of the notebooks in the 3D Reconstruction directory (refer 3D Reconstruction/readme.md for specifics of each notebook)
- Point clouds generated can be downloaded and viewed using softwares like Meshlab


**Clear instructions have been given in notebooks in the 3D reconstruction directory to generate 3D outputs from rgb after finishing the training**

An experimental implementation of the [Bts model](https://arxiv.org/abs/1907.10326) has also been added, which is highly based on https://github.com/cogaplex-bts/bts .


## Demos
**3D PointCloud** (Testset RGB to PointCloud)

Input RGB image from test set - indoor.png <br/>
![input](https://github.com/bsivadatta/3D-image-ReConstruction/blob/master/Demos/3D-demos/indoor.png)

Output PointCloud <br/>
![output](https://github.com/bsivadatta/3D-image-ReConstruction/blob/master/Demos/3D-demos/pointcloud.gif)<br/>

**Video Depth**

Prediction has been done on individual frames of the input video using the model based on mobilenetV2.
![input](https://github.com/bsivadatta/3D-image-ReConstruction/blob/master/Demos/VideoDepth/input.gif)
![output](https://github.com/bsivadatta/3D-image-ReConstruction/blob/master/Demos/VideoDepth/video_depth.gif)

**DepthMap Prediction**

The color rgb part of the picture is the Input RGB and the other half of the picture is our predicted depth map, Darker Pixels are closer.
![1](https://github.com/bsivadatta/3D-image-ReConstruction/blob/master/Demos/DepthMaps/depth_map1.jpeg)

