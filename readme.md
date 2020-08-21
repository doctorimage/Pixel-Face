# Pixel-Face Dataset

##Introduction
We present a large-scale, high-resolution and diverse 3D face dataset, PixelFace, with massive annotations. PixelFace contains a training set with 655 subjects and a validation set with 200 subjects. Each subject has samples under different expressions and multiple views. Each sample provide synchronized multi-view 2D face image, depth(will release in the future), 3D scanning and registration results.There are 8483 samples totally.
The 3D landmarks, age and gender of the subjects are also included. The data have been released to public for non-commercial research purpose.

## Data Downloading  
Dataset Infomation [OneDrive](https://mycuhk-my.sharepoint.com/:f:/g/personal/1155102588_link_cuhk_edu_hk/EpYJzrzBa8FJvx1tZBbSp6IBvHTegO0FNwKzgnZfApCSng?e=FDmTcq), [Baidu Yun](https://pan.baidu.com/s/1U57o2vN8f8E8lfsFynRIjg) 
(Password: tgwx)  
Image & Mesh [OneDrive](https://mycuhk-my.sharepoint.com/:f:/g/personal/1155102588_link_cuhk_edu_hk/EuZzVuao-V9KouJFEqDXFm4BRTsyYWm2kCKTHNyDoSHjAQ?e=zcBRas), [Baidu Yun](https://pan.baidu.com/s/1O-jO4GvsVYNRf4L5hdYi5g) (Password: ve0e)   
Depth: Coming Soon
## Data Description
The available data includes the following.
### 1. information
Download the **Dataset Information** to get folder **release_id/**  
<br>

* release\_id/split/release\_eva.txt and release\_id/split/release\_train.txt  

	The text files containing name of samples for evaluation and training.
	
* release\_id/release_id.txt  
	ids of all data samples

	
* release\_id/release_info.txt

	A text file containing the ages and gender of the subjects. From left to right, each row is the subject, data id, gender (1-male, 0-female), age, and expression label whose detailed definitions are shown in Fig1 (label  0 indicating arbitrary expression which is not defined).
	
	![Fig1. Expression definition.](figures/exp22.png) 
	
	
## 2. Multi-modality Data

There are 8483 multi-modality samples. Each sample consists of: 

1. multi-view 2D images (sample/$VIEW$/t.bmp), the $VIEW$ 0, 1, 2 refer to left, middle, right respectively.
2. 3D scanning and registration results (sample/fusion/gt.mat)
3. multi-view depth (sample/$VIEW$/depth.bmp)

## 3. Tools 
We provide Python3.6 code to extract facial landmarks and obj from the mat file. The instructions of basic setup are:

* Install basic requirements:

	```
	pip install -r requirement.txt 
	```

* Run the following command will extract sample data from .mat and generate .obj files for face meshes. You can follow the same practice to extract other data after downloading.  
```
	python util/read_data.py
```	
