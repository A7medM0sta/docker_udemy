

---

#  Soccer AI 🧠
## Demo
<p align="center">
  <img src="assets/outputs/1.png" alt="Image 1" width="400"/> 
  <img src="assets/outputs/2.png" alt="Image 2" width="400"/>
  <img src="assets/outputs/3.png" alt="Image 3" width="400"/>
  <img src="assets/outputs/4.png" alt="Image 4" width="400"/>
</p>

Link to the [Demo](https://github.com/A7medM0sta/soccer/blob/main/data/2e57b9_0-radar.mp4)
## 📝 Overview
Research and development of AI models for soccer analytics and insights. This project aims to provide tools for detecting players, goalkeepers, referees, and the ball in soccer videos. It also includes features for tracking player movements, classifying players into teams, and visualizing player positions on the soccer field.
### Train ball detectors
<p align="center">
  <div style="display: inline-block; margin: 10px;">
    <p><strong>Train Results</strong></p>
    <img src="assets/img_1.png" alt="Train Results" width="400"/>
  </div>
  <div style="display: inline-block; margin: 10px;">
    <p><strong>Confusion Matrix</strong></p>
    <img src="assets/img.png" alt="Confusion Matrix" width="400"/>
  </div>
  <div style="display: inline-block; margin: 10px;">
    <p><strong>Result for Validation</strong></p>
    <img src="assets/img_2.png" alt="Result for Validation" width="400"/>
  </div>
</p>

### Train player detectors
<p align="center">
  <div style="display: inline-block; margin: 10px;">
    <p><strong>Train Results</strong></p>
    <img src="assets/img_3.png" alt="Train Results" width="400"/>
  </div>
  <div style="display: inline-block; margin: 10px;">
    <p><strong>Confusion Matrix</strong></p>
    <img src="assets/img_5.png" alt="Confusion Matrix" width="400"/>
  </div>
  <div style="display: inline-block; margin: 10px;">
    <p><strong>Result for Validation</strong></p>
    <img src="assets/img_4.png" alt="Result for Validation" width="400"/>
  </div>
</p>

### train pitch keypoint detectors
<p align="center">
  <div style="display: inline-block; margin: 10px;">
    <p><strong>Train Results</strong></p>
    <img src="assets/img_6.png" alt="Train Results" width="400"/>
  </div>
  <div style="display: inline-block; margin: 10px;">
    <p><strong>Result for Validation</strong></p>
    <img src="assets/img_7.png" alt="Result for Validation" width="400"/>
  </div>
</p>

* Developed and integrated Soccer AI using YOLOv8, achieving over 95% precision and 85% recall in player detection, and 99% precision and recall in keypoint detection for real-time soccer game analysis.
## 💻 Installation Guide

We don't have a Python package yet, but you can install from the source in a [**Python>=3.8**](https://www.python.org/) environment. Follow the steps below:

```bash
pip install https://github.com/A7medM0sta/soccer.git
pip install -r requirements.txt
./setup.sh
```


## ⚙️ Modes

### 🏟️ Pitch Detection
Detects the soccer field boundaries and key points in the video. Useful for identifying and visualizing the layout of the soccer pitch.

```bash
python main.py --source_video_path data/2e57b9_0.mp4 --target_video_path data/2e57b9_0-pitch-detection.mp4 --device mps --mode PITCH_DETECTION
```


### 🧑‍🤝‍🧑 Player Detection
Detects players, goalkeepers, referees, and the ball in the video. Essential for identifying and tracking the presence of players and other entities on the field.

```bash
python main.py --source_video_path data/2e57b9_0.mp4 --target_video_path data/2e57b9_0-player-detection.mp4 --device mps --mode PLAYER_DETECTION
```

### ⚽ Ball Detection
Detects the ball in the video frames and tracks its position. Useful for following ball movements throughout the match.

```bash
python main.py --source_video_path data/2e57b9_0.mp4 --target_video_path data/2e57b9_0-ball-detection.mp4 --device mps --mode BALL_DETECTION
```

### 🏃‍♂️ Player Tracking
Tracks players across video frames, maintaining consistent identification. Useful for following player movements and positions throughout the match.

```bash
python main.py --source_video_path data/2e57b9_0.mp4 --target_video_path data/2e57b9_0-player-tracking.mp4 --device mps --mode PLAYER_TRACKING
```


### 🏳️‍ Team Classification
Classifies detected players into their respective teams based on their visual features. Helps differentiate between players of different teams for analysis and visualization.

```bash
python main.py --source_video_path data/2e57b9_0.mp4 --target_video_path data/2e57b9_0-team-classification.mp4 --device mps --mode TEAM_CLASSIFICATION
```



### 🎯 Radar Mode
Combines pitch detection, player detection, tracking, and team classification to generate a radar-like visualization of player positions on the soccer field. Provides a comprehensive overview of player movements and team formations.

```bash
python main.py --source_video_path data/2e57b9_0.mp4 --target_video_path data/2e57b9_0-radar.mp4 --device mps --mode RADAR
```



---





## References
* http://roboflow.com
* https://github.com/roboflow/notebooks/blob/main/notebooks/train-yolov8-object-detection-on-custom-dataset.ipynb
* https://github.com/roboflow/notebooks
* https://blog.roboflow.com/camera-calibration-sports-computer-vision/* 
* https://blog.roboflow.com/tracking-ball-sports-computer-vision/