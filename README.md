# Gazelle Gaze Tracking Video Pipeline

This project implements a **video-based gaze estimation pipeline** using the **Gazelle gaze prediction model** combined with **face detection** to determine where a person in a video is looking.

The system processes a video frame-by-frame, detects faces, predicts gaze direction using a deep learning model, and overlays gaze vectors onto the video.

---

WORKFLOW

<img width="465" height="979" alt="image" src="https://github.com/user-attachments/assets/a6fcfb75-c842-47df-8c63-63ade0d1facd" />


# Project Overview

The pipeline performs the following steps:

1. Load a video input  
2. Detect faces using **RetinaFace**  
3. Normalize bounding boxes for model input  
4. Run gaze prediction using **Gazelle (DINOv2 ViT-L)**  
5. Generate gaze heatmaps  
6. Draw gaze direction arrows on the frame  
7. Save the processed frames to a new video  

---

# Example Output

The output video includes:

- Face bounding boxes  
- Gaze direction arrows  
- Gaze target points  
- In-frame confidence score  

---

# System Architecture
```

Video Input
↓
Frame Extraction (OpenCV)
↓
Face Detection (RetinaFace)
↓
Bounding Box Normalization
↓
Gazelle Model (DINOv2 ViT-L)
↓
Heatmap Prediction
↓
Gaze Vector Visualization
↓
Processed Video Output

```


---

# Technologies Used

- Python  
- PyTorch  
- OpenCV  
- RetinaFace  
- Gazelle gaze model  
- DINOv2 Vision Transformer  
- PIL (image processing)  
- FFmpeg (video encoding)  

---

# Installation

Clone the repository:

```bash
git clone https://github.com/Rithan377/GAZE-Estimation.git
cd GAZE-Estimation
pip install -r requirements.txt

```
<img width="1881" height="1267" alt="image" src="https://github.com/user-attachments/assets/e39eee5b-ae8d-4e22-9d2b-da2967536b8c" />


