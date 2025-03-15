## Introduction

This project is a face recognition-based attendance system using OpenCV and the `face_recognition` library. It detects and identifies faces in real time and logs attendance with timestamps.

## Features

- Detects and recognizes faces in real time using a webcam.
- Matches detected faces with stored images.
- Records attendance with timestamps in a CSV file.
- Uses OpenCV for image processing and `face_recognition` for facial recognition.

## Requirements

Ensure you have the following dependencies installed:

```bash
pip install opencv-python numpy face-recognition
```

## File Structure

- `facerecognitioncode.py` - Main script for real-time face recognition and attendance marking.
- `basics.py` - Basic script to compare two images for facial recognition.
- `images/` - Folder containing stored images of known individuals.
- `Attendance.csv` - File where attendance records are stored.

## How to Use

### 1. Prepare Images

- Place images of individuals to be recognized in the `images/` directory.
- Ensure the filenames match the person's name (e.g., `elon_musk.jpg`).

### 2. Run the Script

- Start the recognition system using:

  ```bash
  python facerecognitioncode.py
  ```

- The system will detect faces through the webcam and match them with stored images.

### 3. Attendance Logging

- Recognized individuals' names will be recorded in `Attendance.csv` along with the timestamp.

## How It Works

1. Loads all images from the `images/` directory and encodes the faces.
2. Captures video frames from the webcam.
3. Detects faces and computes facial encodings.
4. Compares detected faces with known encodings.
5. If a match is found, the name is displayed on the video feed and recorded in `Attendance.csv`.

## Notes

- Ensure all images in `images/` are clear and well-lit for better accuracy.
- You can modify the `markAttendance()` function to include additional details like date or ID.

![Recognition](/TRIAL.jpg)

![Attendance](/AttendanceSheet.png)
