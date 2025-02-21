# Drowsiness Detection System

## Overview
This project implements a real-time drowsiness detection system using OpenCV and Haar cascades. It monitors the user's eyes through a webcam and alerts them if signs of drowsiness are detected.

## Features
- Detects faces and eyes using Haar cascades.
- Tracks blinking rate.
- Identifies when the user's eyes are closed for an extended period.
- Displays status messages such as "Active", "Eyes Closing...", and "DROWSY!".
- Provides an alert if drowsiness is detected.

## Requirements
Make sure you have the following dependencies installed before running the program:

- Python 3.x
- OpenCV (`cv2`)
- NumPy

Install dependencies using:
```bash
pip install opencv-python numpy
```

## Usage
1. Clone this repository:
```bash
git clone https://github.com/yourusername/drowsiness-detection.git
cd drowsiness-detection
```
2. Run the script:
```bash
python drowsiness_detection.py
```
3. The webcam will start capturing frames, and the program will analyze eye movements.
4. Press 'q' to exit the program.

## How It Works
1. The script initializes the webcam and loads pre-trained Haar cascade models for face and eye detection.
2. It detects the face and extracts the eye region.
3. If eyes remain closed for more than 1.5 seconds, an alert is displayed.
4. The blink rate is also monitored and updated every minute.

## Customization
- Modify `DROWSY_TIME_THRESHOLD` to change the duration before a drowsiness alert is triggered.
- Adjust `MIN_EYE_AREA` to refine eye detection sensitivity.

## Limitations
- Performance may vary based on lighting conditions and camera quality.
- Haar cascades may not work as accurately on different face orientations.

## Future Enhancements
- Implement deep learning models for more accurate eye state detection.
- Add an audio alert when drowsiness is detected.
- Optimize performance for real-time applications.

## License
This project is open-source and available under the MIT License.

