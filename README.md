# 🎯 Concentration Tracker

A real-time attention monitoring system that tracks a user's **gaze**, **blinking**, and **head pose** using **MediaPipe** and **OpenCV**. Ideal for study sessions, productivity apps, or screen monitoring tools.

---

## ✨ Features

- 👁️ **Eye Blink Detection**  
  Uses Eye Aspect Ratio (EAR) to detect blinks and prolonged eye closures.

- 👀 **Gaze Estimation**  
  Determines whether the user is looking straight or away using iris landmarks.

- 🧠 **Head Pose Estimation**  
  Measures user head orientation using nose position relative to the screen.

- 📊 **Concentration Score**  
  Calculates attention percentage using weighted factors of blink, gaze, and head pose.

- ⚠️ **Distraction Detection**  
  Counts how often the user is not paying attention and issues visual alerts.

- 💡 **Live UI Feedback**  
  Real-time overlay shows:
  - Concentration %
  - Blinking alert
  - ACTIVE / DISTRACTED indicator
  - Distraction counter
  - FPS display

---

## 🧪 How It Works

1. **Face Mesh**: MediaPipe detects 468 facial landmarks.
2. **EAR**: Eye landmarks compute blink status.
3. **Gaze Score**: Iris center position checks if user is looking forward.
4. **Head Pose Score**: Nose distance from center estimates alignment.
5. **Composite Score**:  
   \[
   \text{Score} = 0.4 \times \text{Gaze} + 0.4 \times \text{Head Pose} + 0.2 \times (1 - \text{Blinking})
   \]

---

## 🖥️ Tech Stack

- Python 3.11
- OpenCV
- MediaPipe
- NumPy
- Deque (for smoothing score history)

---

## 🚀 Getting Started

### 1. Clone this Repository
```bash
git clone https://github.com/asutoshp10/concentration_tracker.git
cd concentration_tracker
