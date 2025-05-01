# signlangdetectionopencv
✋ Hand Gesture Recognition using OpenCV and TensorFlow
A real-time hand gesture recognition system that uses computer vision and a deep learning model to classify hand signs—such as letters and numbers from the sign language alphabet—via a webcam.

📌 Project Overview
This project captures video input from a webcam, detects a hand, extracts the hand region, preprocesses it, and uses a trained Keras model to classify the hand gesture. The result is displayed on-screen with bounding boxes and class labels.

🎯 Objectives
Real-time detection and classification of hand gestures.

Maintain aspect ratio and size consistency using image preprocessing.

Display predictions with high accuracy using a pre-trained neural network.

Enable gesture-based interaction and communication.

🛠️ Technologies Used
Python

OpenCV

TensorFlow / Keras

NumPy

Custom-trained hand gesture classifier


project/
│
├── Model/
│   ├── keras_model.h5       # Trained classification model
│   └── labels.txt           # Class labels (e.g., A-Z, 1-9)
│
├── dat/
│   └── c/                   # (Optional) Collected hand gesture images
│
├── main.py                  # Main application script
└── README.md                # Project documentation







FLOW DIAGRAM


         +-----------------------+
         |   Start Webcam Feed   |
         +----------+------------+
                    |
                    v
         +-----------------------+
         |  Detect Hand using    |
         |  HandDetector Module  |
         +----------+------------+
                    |
            Hand Found? -----> No ----> Loop back to webcam feed
                    |
                   Yes
                    |
                    v
         +----------------------------+
         |  Crop Hand from Frame      |
         |  Add Offset Padding        |
         +-------------+--------------+
                       |
                       v
         +-----------------------------+
         |  Resize Image to 300x300    |
         |  Maintain Aspect Ratio      |
         |  Center on White Canvas     |
         +-------------+---------------+
                       |
                       v
         +-----------------------------+
         |  Classify Gesture using     |
         |  Trained Keras Model        |
         +-------------+---------------+
                       |
                       v
         +-----------------------------+
         |  Display Prediction Label   |
         |  and Bounding Box on Frame  |
         +-------------+---------------+
                       |
                       v
               Loop Until Exit


