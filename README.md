# Face and Eye Detection

A lightweight Flask application that uses OpenCV Haar cascades to detect faces and eyes from a live webcam stream in real time.

This project is designed as a simple computer vision demo and is useful for learning how webcam-based object detection works in Python.

## Features

- Live webcam streaming in the browser
- Real-time face detection
- Real-time eye detection within detected faces
- Simple Flask web interface
- Lightweight and easy to run locally

## Tech Stack

- Python 3
- Flask
- OpenCV
- HTML/CSS

## Project Structure

```text
face-eye-detection/
├── app.py
├── requirements.txt
├── Haarcascades/
│   ├── haarcascade_car.xml
│   ├── haarcascade_eye.xml
│   ├── haarcascade_frontalface_default.xml
│   └── haarcascade_fullbody.xml
├── static/
│   └── style/
│       └── style.css
├── templates/
│   └── index.html
├── myvenv/
│   └── (local virtual environment)
└── README.md
```

## Prerequisites

Before running the project, ensure you have:

- Python 3.9+
- A working webcam connected to your computer
- Access to a modern browser

## Installation

1. Clone the repository or open the project folder.
2. Create and activate a virtual environment:

```bash
python -m venv myvenv
```

On Windows:

```bash
myvenv\Scripts\activate
```

On macOS/Linux:

```bash
source myvenv/bin/activate
```

3. Install the dependencies:

```bash
pip install -r requirements.txt
```

## Running the App

Start the application:

```bash
python app.py
```

Then open your browser and visit:

```text
http://127.0.0.1:5000
```

The page will display a live video feed with blue rectangles around detected faces and green rectangles around detected eyes.

## How It Works

The application:

1. Opens the default webcam using OpenCV
2. Captures frames continuously
3. Uses Haar cascade classifiers to detect faces and eyes
4. Draws bounding boxes around the detected regions
5. Streams the processed frames to the browser via Flask

The key detection files are stored in the Haarcascades folder and are used by OpenCV to identify facial features.

## Notes

- Webcam access must be allowed by the operating system and browser.
- A real camera is required; this app does not work without one.
- The app runs in local development mode with Flask debug enabled.
- The project is meant for demonstration and learning purposes.

## Future Improvements

Possible upgrades include:

- Eye blink detection
- Face landmark tracking
- Emotion recognition
- Better UI design and controls
- Deployment to a web server or cloud environment

## License

This project does not currently include a formal license file. It is intended for educational and personal use unless otherwise specified by the owner.
