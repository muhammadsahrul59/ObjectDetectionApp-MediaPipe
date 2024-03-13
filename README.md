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

## Run the notebook only on Google Colab
```
- Download the file above
- open https://colab.research.google.com/
- Upload the file notebook_objectdetection.ipynb
```

or you can open it with this Google Colab Link below :

[![](https://img.shields.io/badge/Google%20colab-Open-FFC000.svg?style=for-the-badge&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAA4AAAAOCAMAAAAolt3jAAAABGdBTUEAALGPC/xhBQAAACBjSFJNAAB6JgAAgIQAAPoAAACA6AAAdTAAAOpgAAA6mAAAF3CculE8AAAB8lBMVEUAAAD/7QL/6w7/6gz/6w3/6Qj/6Qj/6wj/6gf/6w//6w7/6xP/7gP/2hr/2xX/2jD/z0j/uHX/1zn/3Sz/3Sv/1zn/r4L/zE3/2jL/4ST/4Cf/0RP//zH/3S//2jL/2jL/2zH/3iv/3in/2zD/2jL/2jL/3C///0b/1B3/yxL/xAj/0SH/2DT/2TX/2TX/3C7/2jP/2DX/2DX/2DX/1zD/zRb/YwD/wgf/wQf/xAr/1iX/3C//3C//2zH/2Db/2jP/3C7/2zD/zBf/wgj/wgf/wgf/wQf/wQf/0ST/2y7/5B3/2TT/2TT/3iv/2y//zSD/wQb/wQf/wgf/wgf/wQf/wQf/zx7/3Cz/4x//2TT/2TX/4TD/zRb/wQf/wgf/wQf/wgf/wgf/wQf/wwr/1iT/3S//3C7/2zH/1zH/zBb/wQT/wgf/wQf/wQf/wgf//4r/xAj/0CD/2DT/2TX/2TX/3C7/zBb/wgj/wQf/wQf/wQf/wgf/xgf/0BL/6Rz/3C//2jL/2jP/2zH/3iz/vwD/wgf/wgf/wgf/wgf/xAf/wgf/2Rr/2hf/2TH/t3f//wD/1D//3S7/wgX/wAf/0wj/uQf/wQf/wwf/wgf/5gX/5h//6BT/5xb/6Q//6RD/xAf/xAf/xQf/xAf/xQf/xAf///9tAmifAAAApXRSTlMAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAATiFmGgWFGaZi0EDAABa6v/5+32y//r/8WoBJ9viYD9wnv+kPlvc5TRg/XsAAArH4yEAAGz+cmL9dgAACsjhHgAAZ/50LOHcUzRbm/+VLUjT6TcAZvH89Pd5uv/x+fRxAgADRJSldRsYcKOVSAQAAAAAAAEAAAAAAQAAAAAAAAAAAAAAAAAAAABydb0CAAAAAWJLR0SlLrlKLwAAAAd0SU1FB+QIEQUaC7jgabcAAAABb3JOVAHPoneaAAAAwUlEQVQI12NgQAOMTMwsrGzsHJxc3DwMDLx8/AKCQsIiomLiEpJSDNIysnLyCopKyiqqauoaDJpa2jq6evoGhkbGJqZmDOYWllbWNrZ29g6OTs4uDK5u7h6eXt4+vn7+AYFBDMEhoWHhEZFR0TGxcfEJDIlJySmpaekZmVnZObl5DPkFhUXFJaVl5RWVVdU1DLV19Q2NTc0trW3tHZ1dDN09vX39EyZOmjxl6rTpMxgYZs6aPWfuvPkLFi5avATdAwCl1jTbaxUL4wAAAF5lWElmSUkqAAgAAAADABIBAwABAAAAAQAAADEBAgANAAAAMgAAAGmHBAABAAAAQAAAAAAAAABQaG90b3MgMi43LjAAAAIAAqAJAAEAAADTAAAAA6AJAAEAAADTAAAAAAAAAJOs9JgAAAAldEVYdGRhdGU6Y3JlYXRlADIwMjAtMDgtMTdUMDU6MjY6MTErMDA6MDBd4jn+AAAAJXRFWHRkYXRlOm1vZGlmeQAyMDIwLTA4LTE3VDA1OjI2OjExKzAwOjAwLL+BQgAAABh0RVh0ZXhpZjpFeGlmSW1hZ2VMZW5ndGgAMjExdjfLjwAAABd0RVh0ZXhpZjpFeGlmSW1hZ2VXaWR0aAAyMTHrqE6dAAAAEnRFWHRleGlmOkV4aWZPZmZzZXQANjTZeQZNAAAAGnRFWHRleGlmOlNvZnR3YXJlAFBob3RvcyAyLjcuMIcagsYAAAAASUVORK5CYII=)](https://colab.research.google.com/drive/1v5bPqnuh7sAW48p5zhUKvDqU3hstJ4VM?usp=sharing)
