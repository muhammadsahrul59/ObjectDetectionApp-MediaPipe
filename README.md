# Object Detection using MediaPipe✨

### Overview

This is a camera app that continuously detects the objects (bounding boxes, classes, and confidence) in the frames seen by your device's back camera, in an image imported from the device gallery,  or in a video imported by the device gallery, with the option to use an [Object Detection](https://drive.google.com/file/d/14WwupKYQNYy6JXnKCqGGPhljXOLCtgWR/view?usp=sharing), and [Animal](https://drive.google.com/file/d/1koQqjJfU-z7lLpMvXxPpkJ7R4YycV6oA/view?usp=sharing) model customization.

Object detection model has 7 classes (face, keyboard, mouse, monitor, laptop, microphone, and xboxcontroller). Animal model has 5 classes (cat, dog, monkey, panda, penguin).

The model files are downloaded by a Gradle script when you build and run the app. You don't need to do any steps to download TFLite models into the project explicitly unless you wish to use your own models. If you do use your own models, place them into the app's *assets* directory.

This application should be run on a physical Android device to take advantage of the physical camera, though the gallery tab will enable you to use an emulator for opening locally stored files.

## Labeling Images
To label images with [Label Studio](https://labelstud.io/guide/install), open the Label Studio web application and create a new project. Then, add the images you want to label to the project.

To label an image, click on the image and then click on the object you want to label. You can then draw a bounding box around the object and add a label. Once you have labeled all of the images in your project, you can export the labels to COCO format.

You can Download the Dataset in this link below :
- Object Detection Dataset : [Click Here](https://drive.google.com/file/d/1xp9BOtbNhxiGlaRTkuQ4Mf9-G8ovr-vV/view?usp=sharing)
- Animal Dataset : [Click Here](https://drive.google.com/file/d/1iyUDiO5xESHjNEKZEP0L-iW66Q1tXL0b/view?usp=sharing)

## Build the demo using Android Studio

### Prerequisites

*   The **[Android Studio](https://developer.android.com/studio/index.html)**
    IDE. This sample has been tested on Android Studio Dolphin.

*   A physical Android device with a minimum OS version of SDK 24 (Android 7.0 -
    Nougat) with developer mode enabled. The process of enabling developer mode
    may vary by device. You may also use an Android emulator with more limited
    functionality.
    
### Building

*   Open Android Studio. From the Welcome screen, select Open an existing
    Android Studio project.

*   From the Open File or Project window that appears, navigate to and select
    the *ObjectDetectionApp-MediaPipe* directory. Click OK. You may
    be asked if you trust the project. Select Trust.

*   If it asks you to do a Gradle Sync, click OK.

*   With your Android device connected to your computer and developer mode
    enabled, click on the green Run arrow in Android Studio.

### Models used

Downloading, extraction, and placing the models into the *assets* folder is
managed automatically by the **download.gradle** file.

### Object Detection App Demo

![obj_detection](https://github.com/muhammadsahrul59/ObjectDetectionApp-MediaPipe/assets/101655285/e71daf71-c64f-4b44-a980-5284faeabefe)

## Run the notebook on Google Colab
```
- Download the file above
- open https://colab.research.google.com/
- Upload the file notebook_objectdetection.ipynb
```

or you can open it with this Google Colab Link below :

<a href="https://colab.research.google.com/drive/1v5bPqnuh7sAW48p5zhUKvDqU3hstJ4VM?usp=sharing" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>
