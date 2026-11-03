# MotionSense AI
### Human Activity Recognition and Pose Analysis Using Computer Vision

## Overview

MotionSense AI is a computer vision-based project designed to detect and classify human physical activities using pose estimation and joint angle analysis.

The system uses MediaPipe Pose Landmarker to identify human body landmarks, calculates important joint angles, and applies rule-based classification to recognize activities such as Running and Sitting.

It also generates visual representations of body movements and produces annotated videos showing detected activities.

## Key Features

- **Human Pose Estimation:** Detects human body landmarks using MediaPipe.
- **Joint Angle Calculation:** Calculates Knee, Hip, and Elbow angles.
- **Activity Recognition:** Classifies human activities into Running, Sitting, and Unknown.
- **Pose Visualization:** Displays detected body joints and skeletal connections.
- **Video Processing:** Merges multiple video clips and processes them frame by frame.
- **Movement Analysis:** Generates graphs showing joint angle variations over time.
- **Annotated Video Output:** Displays detected activity labels and frame numbers on processed videos.

## Technologies Used

| Technology | Purpose |
|---|---|
| Python | Main programming language |
| OpenCV | Video processing and visualization |
| MediaPipe | Human pose estimation |
| NumPy | Numerical calculations |
| Matplotlib | Graphs and data visualization |
| Google Colab | Development environment |

## How It Works

The project follows these main steps:

1. **Video Input:** Takes two video clips containing Running and Sitting activities.
2. **Video Merging:** Combines both videos into one video.
3. **Pose Detection:** MediaPipe detects human body landmarks in each frame.
4. **Keypoint Smoothing:** Applies a moving average to smooth detected keypoints.
5. **Joint Angle Computation:** Calculates Knee, Hip, and Elbow joint angles.
6. **Activity Classification:** Uses predefined rules and joint angle thresholds to classify activities.
7. **Performance Evaluation:** Calculates classification accuracy against the expected video labels.
8. **Visualization:** Generates joint angle graphs and an annotated output video.

## Activity Classes

The system currently supports:

- Running
- Sitting
- Unknown

## Project Structure

```text
MotionSense-AI/
│
├── CV_ASSIGNMENT.ipynb
├── Running.mp4
├── Sitting.mp4
├── merged_video.mp4
├── output_annotated.mp4
├── joint_angles.png
│
└── README.md
```

## Installation

Install the required libraries:

```bash
pip install mediapipe==0.10.35
pip install opencv-python
pip install numpy
pip install matplotlib
```

## How to Run

1. Clone or download the project repository.
2. Open Google Colab.
3. Upload the project notebook.
4. Upload the input videos:
   - Running.mp4
   - Sitting.mp4
5. Execute the notebook cells in sequential order.
6. Wait for pose detection, angle calculation, and activity classification to complete.
7. View the generated graphs and annotated video.

## Output

The project generates:

- Merged video containing both activities.
- Detected human pose landmarks.
- Joint angle analysis graphs.
- Activity classification results.
- Annotated video with activity labels.

## Current Limitations

- Currently supports only Running and Sitting activity classification.
- Uses rule-based classification rather than a trained machine learning classifier.
- Detection performance may vary depending on lighting, camera angle, and visibility of the human body.
- The current implementation processes one person at a time.

## Future Improvements

- Add more human activities such as Walking, Jumping, Standing, and Squatting.
- Implement machine learning or deep learning-based activity classification.
- Support multiple-person pose detection.
- Develop a real-time webcam-based activity recognition system.
- Build a graphical dashboard for activity monitoring.
- Improve classification accuracy and robustness.

## Conclusion

MotionSense AI demonstrates how computer vision and pose estimation can be used to understand human movements and recognize physical activities.

By combining MediaPipe, OpenCV, joint angle computation, and rule-based classification, the system provides a foundation for intelligent human activity recognition and movement analysis.

---

**Project Category:** Computer Vision  
**Programming Language:** Python  
**Core Technologies:** MediaPipe, OpenCV, NumPy, Matplotlib  
**Development Environment:** Google Colab
