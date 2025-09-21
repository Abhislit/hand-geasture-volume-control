
# 🎵 Hand Gesture Volume Control

Control your computer's system volume using hand gestures with OpenCV, Mediapipe, and Pycaw.

## 🚀 Features
- Detects hand using webcam
- Adjusts volume by changing distance between thumb and index finger
- Displays live volume bar and percentage

## 📂 How its works 
How the Project Works

Camera Captures Live Video

Your webcam continuously captures frames of your hand.

OpenCV (cv2.VideoCapture) is used for this real-time video capture.

Hand Detection Using Mediapipe

Mediapipe’s Hands module detects your hand in each frame.

It identifies 21 landmarks (key points) on your hand, including fingers and joints.

Finger Tracking

The program tracks thumb tip (id 4) and index finger tip (id 8).

Their (x, y) positions are extracted from each frame.

Gesture to Volume Mapping

Calculates the distance between thumb and index finger using the hypotenuse formula:

distance=(x2−x1)2+(y2−y1)2
distance=(x2​−x1​)2+(y2​−y1​)2
