# Object Detection and Action Recognition using Computer Vision

A real-time computer vision project for detecting objects from webcam video using Python and OpenCV. The system is designed mainly for online exam proctoring, where it can identify suspicious situations such as more than one person in the frame or the presence of objects like a mobile phone or book.

## Project Overview

This project uses deep learning-based object detection to monitor a webcam feed in real time. It detects objects such as:

- Person
- Mobile phone
- Book
- Other supported object classes from the model

When suspicious activity is detected, the application displays warning messages such as:

- `More than one Human detected`
- `Mobile Phone detected`
- `No person detected`

The project is inspired by computer vision techniques such as SSD, YOLO, CNN, and OpenCV-based real-time object detection.

## Features

- Real-time webcam-based object detection
- Detects people and common objects
- Supports proctoring use cases
- Displays bounding boxes around detected objects
- Shows confidence score for each detected object
- Alerts when:
  - More than one person is detected
  - A mobile phone is detected
  - No person is detected
- Lightweight implementation using OpenCV and MobileNet SSD

## Technologies Used

- Python
- OpenCV
- NumPy
- MobileNet SSD
- Caffe model files

## Repository Files

```text
Main.py
MobileNetSSD_deploy (1).caffemodel
MobileNetSSD_deploy.prototxt (1).txt
README.md
```

## Model Files

This project uses the MobileNet SSD object detection model.

| File | Description |
|---|---|
| `MobileNetSSD_deploy (1).caffemodel` | Pre-trained MobileNet SSD model weights |
| `MobileNetSSD_deploy.prototxt (1).txt` | Model architecture/configuration file |
| `Main.py` | Main Python script for webcam object detection |

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/your-repository-name.git
cd your-repository-name
```

### 2. Install Required Packages

```bash
pip install opencv-python numpy
```

### 3. Check File Names

Make sure the model file names used inside `Main.py` match the actual file names in your folder.

Current files:

```text
MobileNetSSD_deploy (1).caffemodel
MobileNetSSD_deploy.prototxt (1).txt
```

Recommended cleaner names:

```text
MobileNetSSD_deploy.caffemodel
MobileNetSSD_deploy.prototxt
```

If you rename them, also update the file paths inside `Main.py`.

## How to Run

Run the Python file:

```bash
python Main.py
```

The webcam window will open and start detecting objects in real time.

Press the exit key or close the window to stop the program, depending on the logic implemented in `Main.py`.

## Expected Output

The system displays detected objects with bounding boxes and confidence scores.

Example outputs include:

```text
person: 87%
cell phone: 84%
More than one Human detected
Mobile Phone detected
No person detected
```

## Use Case

The main use case of this project is online exam proctoring. During an online exam, the system can help monitor the candidate through webcam footage and detect suspicious activity, such as:

- More than one person appearing in the camera frame
- Mobile phone usage
- Absence of the candidate
- Presence of books or other unauthorized objects

## Methodology

The system follows these steps:

1. Start webcam video capture.
2. Read frames from the webcam.
3. Pass each frame through the MobileNet SSD object detection model.
4. Detect objects and draw bounding boxes.
5. Check detected object classes.
6. Display warnings for suspicious activity.
7. Continue monitoring until the program is stopped.

## Results

The report shows the following sample detections:

- Person detected
- Person and mobile phone detected
- No person detected
- More than one person detected
- Person and book detected

## Future Enhancements

- Add support for video file input
- Add background noise or audio analysis
- Improve action recognition
- Save suspicious activity logs
- Generate proctoring reports
- Add face recognition for identity verification
- Improve detection accuracy in low-light conditions
- Build a web-based dashboard for monitoring

## Applications

- Online exam proctoring
- Classroom monitoring
- Office surveillance
- Security monitoring
- Restricted object detection
- Real-time video surveillance

## Limitations

- Detection accuracy may reduce in poor lighting
- Webcam quality affects performance
- Objects may be missed if partially hidden
- False positives can occur
- The system depends on the classes supported by the trained model

## Authors

- Nithin Kumar Surineni
- Prem Rathod Khatravath
- Kedarnath Reddy Mulinti
- Ms. M. Siva Swetha Reddy

Department of Computer Science and Engineering  
Institute of Aeronautical Engineering, Hyderabad, Telangana, India

## References

This project is based on concepts from:

- SSD: Single Shot MultiBox Detector
- MobileNets: Efficient Convolutional Neural Networks for Mobile Vision Applications
- OpenCV-based real-time object detection
- Computer vision-based online proctoring systems

## License

This project is created for academic and learning purposes. You may update this section with your preferred license, such as MIT License.
