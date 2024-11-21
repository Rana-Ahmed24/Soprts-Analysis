# Padel Tennis Tracker

## Introduction

The Padel Tennis Tracker is a system designed to track players and ball movements in a padel game using computer vision techniques. The tracker uses machine learning models for detecting and tracking the ball and players, and outputs annotated video frames for visualization.

## Installation

To use the Padel Tennis Tracker, follow these steps:

1. Clone this repository:
   ```bash
   git clone https://github.com/your-repo/padel-tennis-tracker.git
   cd padel-tennis-tracker
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

### Ball Tracker

The Ball Tracker class is responsible for detecting the ball and interpolating its position when it's not detected. It also identifies frames where the ball is shot based on changes in its vertical position.

### Player Tracker

The Player Tracker class tracks the movement of players on the court. It uses a YOLO-based model to detect players in each frame of the video. The system then filters and selects the players based on their proximity to specific court keypoints.

## Visualization

### 1. **Padel Tracker Visualization Example**

Here is an example of the output produced by the system. The input frame shows a snapshot from the video, with players and the ball being detected and tracked by the system. The bounding boxes are drawn around the detected players and ball.

![Padel Tracker Visualization](https://github.com/your-repo/padel-tennis-tracker/blob/main/images/padel_tracker_example.png)

---

### Notes

- The system relies on the YOLO model for object detection and tracking.
- Ball position interpolation is performed using pandas, ensuring smooth movement even when the ball is temporarily out of frame.

---

