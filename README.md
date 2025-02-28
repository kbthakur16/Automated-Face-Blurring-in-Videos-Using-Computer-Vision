# Automated Face and Object Blurring

## Overview
This project demonstrates real-time face and object detection with automatic blurring using two different approaches:

1. **Face Detection & Blurring using MediaPipe**
2. **Object Detection & Blurring using YOLO (Ultralytics)**

Both scripts process a video feed, detect relevant entities, and apply a blur effect to anonymize detected faces or objects.

---

## Requirements
Ensure you have the following dependencies installed before running the scripts:

- Python
- OpenCV (`cv2` library)
- MediaPipe (for face detection)
- Ultralytics (for YOLO object detection)
- YOLO model weights

You can install the required dependencies using:
```sh
pip install opencv-python mediapipe ultralytics
```

---

## Face Detection & Blurring (MediaPipe)
### Description:
- The script utilizes **MediaPipe Face Detection** to detect faces in video frames.
- Detected faces are highlighted with bounding boxes and blurred for privacy.
- The processed frames are displayed and saved to an output video file.

### Usage:
Run the script with a video file as input:
```sh
python face_blur.py --input input_video.mp4 --output output_video.mp4
```
Press `q` to exit the live preview.

---

## Object Detection & Blurring (YOLO)
### Description:
- The script employs **YOLOv8** (via Ultralytics) for object detection.
- Objects detected in each frame are boxed and blurred.
- Supports real-time processing and video file input.

### Usage:
Run the script with the required model weights and video file:
```sh
python object_blur.py --input input_video.mp4 --output output_video.mp4 --weights yolov8n.pt
```
Press `q` to exit the live preview.

---

## Output
Both scripts generate an output video file (`output_video.mp4`) containing the processed video with faces or objects detected and blurred.

---

## Notes
- You can adjust confidence thresholds and detection models as needed.
- Ensure the correct YOLO weights (`yolov8n.pt`) are available before running the object detection script.

---

## License
This project is open-source and available under the MIT License.

---

## Contributing
Pull requests and suggestions are welcome! Feel free to enhance the detection models, optimize processing, or add new features.

---

## Contact
For any questions, feel free to raise an issue or reach out.

---

Enjoy building privacy-focused video processing applications! 🚀
