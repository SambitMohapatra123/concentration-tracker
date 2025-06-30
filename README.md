# concentration-tracker
The Concentration Tracker is a real-time system that uses MediaPipe and OpenCV to monitor focus by analyzing eye blinks, gaze direction, and head pose. It calculates a concentration score, shows it with a visual bar, and tracks distractions using facial landmarks from webcam input.
# 🧠 Real-Time Concentration Tracker

The **Concentration Tracker** is an intelligent real-time system designed to monitor and analyze user attention levels through a standard webcam. It combines advanced computer vision techniques using **MediaPipe Face Mesh** and **OpenCV** to evaluate visual focus based on facial cues like eye activity, gaze direction, and head pose.

## 🔍 Overview
This project aims to assess user concentration by:
- Detecting eye blinks using **Eye Aspect Ratio (EAR)**
- Tracking gaze using **iris landmarks**
- Evaluating head pose based on **nose alignment**
- Calculating a **concentration score** (0–100%) in real time
- Displaying focus status with a visual bar and alerts

If the user consistently shows signs of distraction, the system activates a **distraction counter** and triggers alert logic when thresholds are crossed.

## 💡 Key Features
- 🎯 **Real-time Attention Scoring**  
  Calculates concentration score using weighted metrics.

- 👀 **Blink & Gaze Detection**  
  Uses facial landmarks and iris position to monitor eye activity and gaze direction.

- 🧭 **Head Pose Estimation**  
  Measures nose position relative to screen center to detect orientation.

- 📊 **Smooth Scoring & Visualization**  
  Uses a moving average (deque) to stabilize score output; displays a progress bar with visual cues.

- 🚨 **Distraction Alert System**  
  Tracks periods of inattention and triggers reset or alert after defined limits.

## ⚙️ Technologies Used
| Library     | Purpose                                  |
|-------------|------------------------------------------|
| OpenCV      | Video capture, drawing, image handling   |
| MediaPipe   | 3D face mesh and iris landmark tracking  |
| NumPy       | Mathematical operations (distances)      |
| Python Deque| Smoothing score over time                |

## 📦 Applications
- Online learning platforms (student focus monitoring)
- Workplace productivity and screen time analytics
- Driver alertness systems
- Human behavior or psychological studies

## 🖼️ Example Output
- **Concentration Score:** `Concentration: 87%`
- **Status Indicator:** `ACTIVE` / `DISTRACTED`
- **Blink Detection:** "BLINKING"
- **Distraction Counter:** "Distraction: 5"
- Real-time **colored progress bar**
