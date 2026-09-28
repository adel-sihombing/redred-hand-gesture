# REDRED — Gesture Recognition Camera ❤️💚

A small computer vision project inspired by **“REDRED” by CORTIS**.

This project uses a real-time webcam to recognize static hand gestures and create different visual responses based on the detected gesture.

## Inspiration

This project was inspired by CORTIS' **“REDRED”**, from their 2nd EP **[GREENGREEN]**.

The red and green concept inspired me to experiment with translating hand gestures into a simple interactive visual experience.

## Features

- Real-time hand detection using a webcam
- Hand landmark tracking with MediaPipe
- Gesture recognition
- Interactive red/green visual response
- Neon-green hand skeleton with yellow joints
- Built with Python

There are two main gestures:

- 🖐️ **RED RED** — Hold up both hands as open palms facing the camera. The screen turns red at 50% transparency and a large `RED RED` label appears in the center.
- 🤘 **GREEN GREEN** — Make the metal (rock) sign with both hands. The screen turns green at 50% transparency with a large `GREEN GREEN` label.

## Concept

The project connects simple hand gestures with the **RED / GREEN** visual concept from the inspiration.

> REDRED ❤️  
> A small project inspired by music, creativity, and computer vision.

## How It Works

- MediaPipe HandLandmarker, a pre-trained model, detects **21 landmarks per hand** in each frame.
- Gestures are detected using simple geometric rules based on those landmarks.
- No additional training is required.
- Palm-vs-back-of-hand detection uses 2D geometric calculations combined with handedness.

While the hands are being tracked, they are displayed on screen as a neon-green skeleton with yellow joints.

Press **ESC** or **q** at any time to quit.

## Built With
- Python
- OpenCV
- MediaPipe
- NumPy

## Requirements
- Python 3.11 or later
- A webcam
- Packages listed in `requirements.txt`:
  - `mediapipe`
  - `opencv-contrib-python`
  - `numpy`
- The `hand_landmarker.task` model file
  
### Option A — Using uv

```bash
uv venv
uv pip install -r requirements.txt
