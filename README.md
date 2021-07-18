# Vehicle-Classification-Using-OpenCV
This repository contains my project files for my summer project on Vehicle Classification using OpenCV and YOLOv4. This project detects vehicles in an image/video and classifies them into 8 categories: Car,Bus,Truck,Van,Motorcycle,Bicycle,Person,Auto-Rickshaw. To use this project simply follow the steps in the file Run_Detections_Darknet.ipynb or clone the repository on your local machine and run the Yolov4_Inference.py on it if it satisfies all the requirements.


<p align="center">
  <img src="https://user-images.githubusercontent.com/83576606/126082146-f90999eb-2511-40e8-9a0d-66f5cbcb7869.png" width="50%" height="50%">
  <img src="https://user-images.githubusercontent.com/83576606/126082468-fe3770af-9af0-4d98-b1b5-0198ca3b027b.png" width="50%" height="50%">
  <img src="https://user-images.githubusercontent.com/83576606/126082545-d5fcd22d-a8b2-40a5-9b1f-8a46d097494e.png" width="75%" height="75%">
</p>

## Darknet and YOLOv4
The Darknet is an open-source neural network framework written in C and CUDA and serves as the basis of YOLO. It is fast, easy to install, and supports CPU and GPU computation. Darknet is used as the framework for training YOLO. YOLO can predict the class of object, its bounding box, and the probability of the class of object in the bounding box.<br/>


<p align="center">
  <img src="http://pjreddie.com/media/files/darknet-black-small.png">
</p>

## Features Of Project
* Trained on total 15326 images of Car,Bus,Truck,Van,Motorcycle,Bicycle,Person from the Open Images Dataset. Since the Open Images Dataset(OID) does not contain the class auto-rickshaw, the images for auto-rickshaw class were manually gathered and processed into YOLO format and added to the dataset.
* Training parameters used: width=416,height=416, max_batches = 16000, steps=(12800,14400), filters = 39
* Maximum mAP(Mean Average Precision) score that was achieved: 74.56%
* Maximum IoU(Intersection over Union) score that was achieved: 50.41%
* Can be run in cloud using Google Colab.  
Note that since OID doesn't contain any auto-rickshaws and that they were manually added, so they are detected but are classified wrongly due to severe lack of training data compared to other classes.
## Dependencies and Requirements
Before downloading please confirm the versions supported by your computer.
* CMake
* opencv-python
* opencv-contrib-python
* cuDNN
* GPU with CUDA Cores
* Darknet
* YOLOv4 weights


## References
* https://github.com/AlexeyAB/darknet
* https://github.com/theAIGuysCode/OIDv4_ToolKit.git
* https://colab.research.google.com/drive/1_GdoqCJWXsChrOiY8sZMr_zbr_fH-0Fg?usp=sharing (credits: AI GUY)
* https://gist.github.com/YashasSamaga/e2b19a6807a13046e399f4bc3cca3a49
