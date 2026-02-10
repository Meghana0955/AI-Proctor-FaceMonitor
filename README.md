
AI Proctor Face Detector

AI Proctor Face Detector is a real-time face monitoring module designed for secure online interviews and remote assessments. The system uses computer vision techniques to detect face presence, absence, and multiple faces, helping prevent cheating and impersonation.

This module is part of a larger AI-powered secure interview monitoring system.

Features

Real-time face detection using webcam

Detects when candidate leaves the screen

Detects multiple faces in the frame

Visual warning system

Lightweight and fast

Uses pretrained AI models (no training required)

Demo Behavior
Situation	System Output
One face detected	Normal
No face detected	Face Missing
Multiple faces detected	Warning: Multiple Faces Detected
Technologies Used

Python

OpenCV

MediaPipe Face Landmarker

Project Structure
AI-Proctor-FaceMonitor/
│
├── face_detection.py
├── requirements.txt
├── .gitignore
└── README.md

Installation
Step 1: Clone the repository
git clone https://github.com/your-username/AI-Proctor-FaceMonitor.git
cd AI-Proctor-FaceMonitor

Step 2: Create a virtual environment
python -m venv env


Activate the environment:

Windows:

env\Scripts\activate


Mac/Linux:

source env/bin/activate

Step 3: Install dependencies
pip install -r requirements.txt

Running the Face Detection System
python face_detection.py


Press q to exit the webcam window.

How It Works

The system captures real-time video from the webcam.

A pretrained MediaPipe face detection model processes each frame.

The system counts the number of faces detected.

Based on the count, it classifies the situation:

No face → Face Missing

One face → Normal

Multiple faces → Warning

Example Output Logic
if face_count == 0:
    status = "Face Missing"
elif face_count == 1:
    status = "Normal"
else:
    status = "Multiple Faces Detected"

Use Cases

Online job interviews

Remote proctoring systems

Online examinations

Identity verification systems

Secure remote assessments

Future Improvements

Eye tracking integration

Voice activity detection

Network behavior monitoring

Cheating risk scoring system

Encrypted data transmission

Interviewer dashboard

Author

Your Name
Final Year Project
AI-Powered Secure Interview Monitoring System

License

This project is for educational and research purposes.
You may modify and use it for academic or personal projects.
