
# Face Detection Using OpenCV

This project implements real-time face detection using OpenCV's Haar Cascade Classifier on webcam feed. The program continuously captures frames from the webcam and detects faces, displaying a message indicating whether a face has been detected or not. When faces are detected, the program highlights them with a bounding box.

## Prerequisites

Before running the project, ensure you have the following installed:

- Python 3.x
- OpenCV library (`opencv-python`)

You can install OpenCV by running the following command:

```bash
pip install opencv-python
```

Additionally, you need to download the Haar Cascade Classifier file for frontal face detection:

- [haarcascade_frontalface_default.xml](https://github.com/opencv/opencv/tree/master/data/haarcascades)

## How It Works

1. The program captures the video stream from the webcam using `cv2.VideoCapture`.
2. The captured frames are converted to grayscale.
3. A Haar Cascade Classifier model is used to detect faces in each frame.
4. If a face is detected, a bounding box is drawn around the face, and a message `Face Detected!` is displayed.
5. If no face is detected, the message `No Face Detected!` is shown instead.
6. Press **Esc** to exit the program.

## File Structure

```
.
├── haarcascade_frontalface_default.xml   # Haar Cascade Classifier XML for face detection
└── face_detection.py                     # Python script for face detection using OpenCV
```

## Usage

1. Ensure that the `haarcascade_frontalface_default.xml` file is located in the appropriate directory.
2. Run the Python script:

```bash
python face_detection.py
```

3. The webcam window will open. If a face is detected, it will display a message on the screen, and the detected face will be surrounded by a bounding box. Otherwise, it will display `No Face Detected!`.
4. Press the **Esc** key to stop the program and close the webcam window.

## Code Explanation

- **Video Capture**: The program uses `cv2.VideoCapture(0)` to capture the webcam feed.
- **Face Detection**: `CascadeClassifier.detectMultiScale()` detects faces in each frame.
- **Face Detection Feedback**: Displays the message `Face Detected!` or `No Face Detected!` using `cv2.putText()`.
- **Bounding Box**: Draws a green rectangle around the detected face using `cv2.rectangle()`.

