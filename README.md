# README

## Overview

This repository contains two Python scripts demonstrating real-time object and face detection with blurring in video feeds. The first script utilizes the YOLO object detection model via the Ultralytics library to detect and blur objects. The second script employs the MediaPipe library for face detection and blurring.

## Requirements

The following dependencies are required to run the scripts:

- Python
- OpenCV (cv2) library
- Ultralytics library (for object detection)
- YOLO model weights (for object detection)
- MediaPipe library (for face detection)

## Object Detection and Blurring (YOLO)

### Description

- Imports necessary libraries: `os` for file handling, `cv2` for OpenCV, and `YOLO` from Ultralytics.
- Loads the YOLO model using the `YOLO` class and specifies the configuration file (`yolov8n.yaml`).
- Initiates training using the `train` method, specifying the training data configuration (`config.yaml`) and the number of epochs.
- Reads the video file frame by frame using OpenCV's `VideoCapture` class.
- Detects objects in each frame using the YOLO model and applies a blur effect to detected objects.
- Writes processed frames to an output video file using OpenCV's `VideoWriter` class.
- Displays the processed video feed in a window named "Detection" (press 'q' to exit).

### Output

- Generates an output video file named **"Output.mp4"** containing the processed video with objects detected and blurred.

## Face Detection and Blurring (MediaPipe)

### Description

- Imports necessary libraries: `cv2` for OpenCV and `mediapipe` for face detection.
- Defines a function `process_img` to process each video frame, detect faces, draw bounding boxes, and apply a blur effect.
- Reads frames from the input video file, processes each frame using `process_img`, and writes the processed frames to an output video file.
- Initializes the face detection model using the `mp_face_detection.FaceDetection` class, allowing configuration of confidence threshold and model type.
- Displays the processed video feed in a window named "Mediapipe Feed" (press 'q' to exit).

### Output

- Generates an output video file named **"Output.mp4"** containing the processed video with faces detected and blurred.

## Usage

1. Install required dependencies using `pip install opencv-python mediapipe ultralytics`.
2. Run the respective script for object or face detection.
3. Provide an input video file and obtain an output video with detection and blurring applied.

