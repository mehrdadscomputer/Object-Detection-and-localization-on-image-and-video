# Object-Detection-and-localization-on-image-and-video
<img width="361" alt="1" src="https://user-images.githubusercontent.com/4415508/42995249-9db07b40-8c25-11e8-858e-fe4d0f992576.png">
<img width="361" alt="5" src="https://user-images.githubusercontent.com/4415508/42991611-5c4ca2e6-8c1b-11e8-89c8-fc59065ad401.png">
<img width="368" alt="3" src="https://user-images.githubusercontent.com/4415508/42991597-53183c94-8c1b-11e8-909f-a0f39ad22196.png">
Link to channel 3 logo detection using webcam (appology for low quality video)
(https://www.aparat.com/v/Lquak)

## Prerequirement:
- TensorFlow's Object Detection API to train an object detection classifier for multiple objects
- TensorFlow-GPU version 1.5 and newer version
- Windows 10, 8, or 7
- CUDA and cuDNN

## Introduction
The purpose of this tutorial is to explain how to run my convolutional neural network object detection classifier for multiple objects.
At the end of this procedure, you will have a program that can identify and draw boxes around Iran national
TV channel logos (Channel One, Channel Three and Channel Five) in pictures, videos, or in a webcam feed.
I used this tutorial to configure, train and run my DNN: [GitHub Pages](https://github.com/EdjeElectronics/TensorFlow-Object-Detection-API-Tutorial-Train-Multiple-Objects-Windows-10/).

## Steps
### 1. Install TensorFlow-GPU 1.5 (skip this step if TensorFlow-GPU 1.5 is already installed) and other requirements
Install TensorFlow-GPU by following the instructions in .[this YouTube Video by Mark Jay](https://www.youtube.com/watch?v=RplXYjxgZbw)

The video is made for TensorFlow-GPU v1.4, but the “pip install --upgrade tensorflow-gpu” command will automatically download version 1.5. Download and install CUDA v9.0 and cuDNN v7.0 (rather than CUDA v8.0 and cuDNN v6.0 as instructed in the video), because they are supported by TensorFlow-GPU v1.5. As future versions of TensorFlow are released, you will likely need to continue updating the CUDA and cuDNN versions to the latest supported version.

Be sure to install Anaconda with Python 3.6 as instructed in the video, as the Anaconda virtual environment will be used for the rest of this tutorial.
After Anaconda virtual environment installation,
From the Start menu in Windows, search for the Anaconda Prompt utility, right click on it, and click “Run as Administrator”. If Windows asks you if you would like to allow it to make changes to your computer, click Yes.

In the command terminal that pops up, create a new virtual environment called “tensorflow1” by issuing the following command:
```
C:\> conda create -n tensorflow1 pip python=3.5
```
Then, activate the environment by issuing:
```
C:\> activate tensorflow1
```
Install tensorflow-gpu in this environment by issuing:
```
(tensorflow1) C:\> pip install --ignore-installed --upgrade tensorflow-gpu
```
Install the other necessary packages by issuing the following commands:
```
(tensorflow1) C:\> conda install -c anaconda protobuf
(tensorflow1) C:\> pip install pillow
(tensorflow1) C:\> pip install lxml
(tensorflow1) C:\> pip install Cython
(tensorflow1) C:\> pip install jupyter
(tensorflow1) C:\> pip install matplotlib
(tensorflow1) C:\> pip install pandas
(tensorflow1) C:\> pip install opencv-python
```
### 2. Clone this repository
Download the full repository located on this page (scroll to the top and click Clone or Download) and extract all the contents directly into the `C:\Users\[YOUR USER NAME]\Desktop\` directory.

### 3. Use the model to detect and localize
To test object detector, move a picture of the object or objects into the root directory of this repository on your computer. Alternatively, you can use a video of the objects (using Object_detection_video.py), or just plug in a USB webcam and point it at the objects (using Object_detection_webcam.py).
To run any of the scripts, type “idle” in the Anaconda Command Prompt (with the “tensorflow1” virtual environment activated) and press ENTER. This will open IDLE, and from there, in the menu, click on `File` and then click `open` and select one of these scripts according to your need (Object_detection_image.py, Object_detection_video.py and Object_detection_webcam.py). Change the IMAGE_NAME variable in the Object_detection_image.py to match the file name of the picture.
Then in the `menu`, click on Run and then click `Run Module`.

If everything is working properly, the object detector will initialize for about 10 seconds and then display a window showing any objects it’s detected in the image!
