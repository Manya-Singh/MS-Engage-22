# In-browser real-time COCO SSD Object Detector

<img width="620" alt="60ed9a4e09e2c648f1b8a013_object-detection-cover" src="https://user-images.githubusercontent.com/77196311/170873319-e9d94455-75a6-4314-85b7-71483184b502.png">

This repository contains the code needed to build an object detection web app using TensorFlow.js and React. The app, uses the computer's webcam stream to perform real-time object detections in every frame it receives.

## The model

The model featured in the app, is a pre-trained COCO SSD system. It is on the fast-but-less-accurate side of the spectrum of all tensorflow architectures, allowing it to be used in a browser.
COCO refers to the "Common Objects in Context" dataset, the data on which the model was trained on. This collection of images is mostly used for object detection, segmentation, and captioning, and it consists of over 200K labeled images belonging to one of 90 different categories, such as "person," "bus," "zebra," and "tennis racket." SSD, short for Single Shot Detector, is a neural network architecture made of a single feed-forward convolutional neural network that predicts the image's objects labels and their position during the same action. The counterpart of this "single-shot" characteristic is an architecture that uses a "proposal generator," a component whose purpose is to search for regions of interest within an image.
Once the regions of interests have been identified, the second step is to extract the visual features of these regions and determine which objects are present in them, a process known as "feature extraction." COCO-SSD default's feature extractor is lite_mobilenet_v2, an extractor based on the MobileNet architecture. In general, MobileNet is designed for low resources devices, such as mobile, single-board computers, e.g., Raspberry Pi, and even drones.

## Requirements

Only a browser, a local web server and something to show! :-)

## Flowchart 

![flowchart](https://user-images.githubusercontent.com/77196311/170870346-c75f9cbc-bec2-4ce0-96d8-676cb58ac274.jpeg)

## Instructions to launch the App

To launch the web app, 

~ Clone the repository on a laptop or system (not compatible with mobiles, tablets or smartphones), recommended to clone in D drive. For this, open the Command Line Prompt and type

~ D: to get into the D drive of the system

~ git clone <insert URL of the cloned repo>

~ cd <in repo>

~ code . to open the files in VS Code

~ In VS Code, go to package.json -> in its terminal type <npm install> to install all the dependencies

~ Go to App.js in src -> in its terminal, type <npm start> to launch the app on your browser. After a few seconds of compilation, you'll be redirected to a new browser at http://localhost:3000/, and then will be greeted by a prompt window requesting permission to access the webcam. Upon accepting said request, wait a bit until the model is downloaded and voila, rejoice with the glory of out-of-the-box deep learning.

P.S. Possible X-factor: Disco-lighting of the rectangular bounding box surrounding the objects? What does the panel of judges have to say to it? I'm all ears to know that :-))

This is the app in action.
  
![demo4](https://user-images.githubusercontent.com/77196311/170871643-386e9788-a22e-4ae2-91e1-0fd2321ddf44.jpg)

![demo5](https://user-images.githubusercontent.com/77196311/170871658-00603881-9f67-47a2-a653-4990765d9828.jpg)

![demo10](https://user-images.githubusercontent.com/77196311/170871682-f6bcbd8b-ac36-485b-839d-bdbfc0b961ff.jpg)

![demo12](https://user-images.githubusercontent.com/77196311/170871698-2417a37a-af37-4668-b736-afcc1c5129d7.jpg)

![demo13](https://user-images.githubusercontent.com/77196311/170871705-464d17f9-268e-487b-9fcb-3778ef7a5cb2.jpg)

![demo6](https://user-images.githubusercontent.com/77196311/170871717-79b11b80-8c27-4a4b-b924-59b58cabe295.jpg)

![demo8](https://user-images.githubusercontent.com/77196311/170871728-2bc786d8-9dba-4950-a4d6-68c5adc265f3.jpg)


## Background

Object detection - the task of locating one or more objects in an image, drawing bounding boxes around them, and predicting the class of the objects - has been a core challenge in computer vision. The TensorFlow Object Detection API is an open source framework built on top of TensorFlow that makes it easy to construct, train and deploy object detection models.

This framework provides support for several object detection architectures such as SSD (Single Shot Detector) and Faster R-CNN (Faster Region-based Convolutional Neural Network), as well as feature extractors like MobileNet and Inception. The variety in architectures and extractors provides lots of options but deciding on which one to use depends on the use-case - what accuracy and speed is needed.

The multimodal toolkit contains an implementation of real time object detection using the COCO SSD model from tensorflow. The application takes in a video (either through webcam or uploaded) as an input and subsequently identifies all the objects present in each frame.

## Results

To use the real time object detection function, simply select the ‘Real Time Object Detection’ option from the tools page. Once the page loads, ensure that the webcam is enabled and the function will automatically detect all the objects shown in the video frame that has been trained in the COCO-SSD model. An added functionality can be to be able to record a video or upload a video and download data on the objects.




