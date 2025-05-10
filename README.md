# 🚗 Vehicle Counter and Tracker with OpenCV

This project is a Python-based vehicle counting and tracking system using OpenCV. It processes a video input, detects moving vehicles, tracks their paths, and counts how many pass **upward** and **downward** across predefined lines.

---

## 📁 Project Structure

* **`main.py`** – The main script that processes the video, tracks vehicles, and handles line crossing logic.
* **`gadi.py`** – Contains the `Car` and `MultiCar` classes used to store and manage object tracking data.

---

## 🛠 Requirements

Ensure you have Python 3 installed and install dependencies using:

```bash
pip install opencv-python numpy
```

---

## 📹 Input

* A video file named `video demo.mp4` placed in the same directory.
* The script uses OpenCV to capture and process frames from this video.

---

## 🚀 How It Works

1. **Background Subtraction**: Detects moving objects using MOG2.
2. **Contours and Centroid Tracking**: Identifies vehicles by calculating contour areas and centroids.
3. **Line Crossing Detection**:

   * Blue Line: Up direction threshold
   * Red Line: Down direction threshold
   * White Lines: Limits for tracking zone
4. **Object Aging**: Removes old objects no longer in frame.

---

## 📈 Output

* Annotated video frame showing:

  * Detected vehicle bounding boxes
  * IDs of vehicles
* Real-time window showing processed frames.
* Console prints crossing events with timestamps and vehicle IDs.

---

## 🧠 Features

* Assigns unique IDs to each vehicle.
* Detects direction based on centroid motion history.
* Automatically cleans up old/dormant tracked objects.

---

## 🎮 Controls

* Press **Q** to exit the video window.

---

## 🔍 Notes

* Accuracy may vary depending on lighting and video quality.
* For improved performance in production, consider:

  * Object detection models (YOLO, SSD) for better accuracy.
  * Multi-object trackers like Deep SORT.
* You may need to adjust line positions and thresholds for different videos.

---

## 👨‍💻 Author

Developed by **Abhilash**

---
