# 3D-image-understanding-Construction
- Predicting the depth of the objects, construct 3D images from 2D images <br/>
- Work is based on [High Quality Monocular Depth Estimation via Transfer Learning](https://arxiv.org/abs/1812.11941)<br/>
by Ibraheem Alhashim and Peter Wonka<br/>

## DEPTH ESTIMATION
**Dataset**<br/>
[NYU V2](https://tinyurl.com/nyu-data-zip)

**Pretrained models** are available at:<br/>
[PyTorch](https://drive.google.com/file/d/1wvhQhs2CAGumRslknNkPBRCNNKMOHw78/view?usp=sharing)<br/>
[Tensorflow](https://drive.google.com/file/d/1wvhQhs2CAGumRslknNkPBRCNNKMOHw78/view?usp=sharing)<br/>

- Models I trained are available in this [google-drive link](https://drive.google.com/drive/folders/1C88ENnOCOi_5eeusYJcFNieDSWYgawCk?usp=sharing) models have been saved in folders with names in the format "architecturename_shapeofinput_numberofepochs" (full refers to 480x640 input shape)
- Results of each of these models are below.<br/>
- Run the evaluate notebook in evaluate directory using appropriate model and input-size for evaluation.<br/>
- Evaluation was done on the [nyutest_data](https://s3-eu-west-1.amazonaws.com/densedepth/nyu_test.zip) compiled in .npy format.<br/>
- Results obtained <br/>
![results](https://github.com/sivadatta-ss20/3D-image-understanding-Construction/blob/master/results/results.png)<br/>

**Sample output using our MobileNetV2 model on Tensorflow 2.x Have been shown clearly in the Demos Folder**


## 3D from rgb and depth
- Run either of the notebooks in the 3D Reconstruction directory (one uses o3d and is faster, other is slow and customisable and doesnot require any external library)
- Point clouds generated can be downloaded and viewed using softwares like Meshlab

## Training 
- Run the notebook Training.ipynb after you place the "data" folder of the nyu-dataset from the link given above in the same directory as the notebook file.
- Default model is based on MobileNetV2. To train on different models , replace the content in model.py with the codes given in the models directory.

**Clear instructions have been given in the o3d.ipynb notebook in the 3D reconstruction directory to generate 3D outputs from rgb after finishing the training**

An experimental implementation of the [Bts model](https://arxiv.org/abs/1907.10326) has also been added, which is highly based on https://github.com/cogaplex-bts/bts .
