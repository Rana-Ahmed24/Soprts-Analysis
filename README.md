
# Padel Tennis Tracker 🎾  
A video analysis tool for tracking players, the ball, and scoring in Padel Tennis matches. This project leverages **YOLO (You Only Look Once)** models to detect and track objects in real-time.

![Uploading image.png…]()

## Features
- **Player Tracking**: Identifies players on the court and tracks their movements.
- **Ball Tracking**: Detects the ball, interpolates missing positions, and identifies hits.
- **Scoring System**: Automatically updates the scoreboard based on ball movements across the court.
- **Visualization**: Overlays bounding boxes, player IDs, and a live scoreboard on the video.
- **Mini Court**: Displays a scaled-down version of the court for better visualization.

---

## Project Structure
```plaintext
.
├── models/                 # YOLO models for ball and player detection
├── input_videos/           # Input video files
├── output_videos/          # Processed output videos
├── stubs/                  # Stub files for caching detections
├── utils.py                # Helper functions
├── trackers/               # Tracking modules for players and the ball
│   ├── player_tracker.py   # Tracks players across frames
│   └── ball_tracker.py     # Tracks the ball across frames
├── court_line_detector.py  # Detects court lines and keypoints
├── mini_court.py           # Visualizes the mini court
├── constants.py            # Shared constants
├── main.py                 # Main script
└── README.md               # Project documentation
```

---

## Installation
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/padel-tennis-tracker.git
   cd padel-tennis-tracker
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Download pre-trained YOLO models and place them in the `models/` directory.

---

## Usage
1. Place your input videos in the `input_videos/` folder.
2. Run the main script:
   ```bash
   python main.py
   ```
3. Use the Gradio interface to upload a video or select from the `input_videos/` folder.
4. The output video with tracking and scoring will be saved in the `output_videos/` folder.

---

## Visual Workflow

### 1. Input Video
A raw video of a Padel Tennis match is loaded.

![Input Video Example](https://via.placeholder.com/600x300?text=Input+Video)  

---

### 2. Detection and Tracking
- Players are identified and assigned unique IDs.
- The ball's trajectory is tracked and interpolated for missing frames.

![Detection Process](https://via.placeholder.com/600x300?text=Player+and+Ball+Detection)

---

### 3. Scoreboard Overlay
The live scoreboard is updated based on ball movements and displayed on the video.

![Scoreboard Overlay](https://via.placeholder.com/600x300?text=Scoreboard+Overlay)

---

### 4. Mini Court Visualization
A scaled-down version of the court visualizes player and ball positions.

![Mini Court](https://via.placeholder.com/600x300?text=Mini+Court+Visualization)

---

### 5. Output Video
The final video contains:
- Bounding boxes for players and the ball.
- Updated scoreboard.
- Mini court overlay.

![Output Video Example](https://via.placeholder.com/600x300?text=Output+Video)

---

## Customization
- Update `constants.py` to adjust scoring rules or court dimensions.
- Replace YOLO models in the `models/` folder for improved detection accuracy.

---

## License
This project is licensed under the MIT License.

---
