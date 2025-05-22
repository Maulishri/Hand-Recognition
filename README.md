# Hand-Recognition

Identifies the presense of a hand in the frame and identifies the number of fingers being held up.

## Overview

The system uses OpenCV to detect the region of interest (ROI), apply skin color filtering, analyze contours, and identify finger positions based on convex hulls and convexity defects.

---

## Process Breakdown

### 1. **SET**
- Turn the **Camera On**

### 2. **READ**
- Capture an **Available Frame**

### 3. **SET**
- Mark the captured frame as the **First Frame**
- Define the **Region of Interest (ROI)** where the hand is expected

### 4. **CONVERT**
- Convert the image from **BGR** to **HSV** or **Black and White**

### 5. **DEFINE**
- Define the **Skin Color Range** for masking

### 6. **MASK**
- Extract and mask the skin color region
- Apply **Gaussian Blur** for smoothing

### 7. **FIND**
- Detect **All Contours** in the masked image
- Select the contour with the **Largest Area** (presumably the hand)

### 8. **MAKE**
- Construct the **Convex Hull** around the hand
- Measure and define the **Area of the Hand**

### 9. **FIND**
- Identify **Convexity Defects** (gaps between fingers)
- Measure **Distance and Angle** between defect points and the convex hull

### 10. **DO**
- **Ignore** defects with an **Angle > 90°**
- Draw **Boundaries** around the hand and/or fingertips
- **Count the Number of Fingers**

### 11. **PRINT**
- Output the detected **Number of Fingers**
- Decision based on the **Hull Area** and **Defect Nodes**

### 12. **CLOSE**
- **Quit** the camera feed when an **Exit Condition** (e.g., key press) is met

---

# Sample Outputs

<img width="468" alt="image" src="https://github.com/user-attachments/assets/6fc43649-2bbd-4abe-b271-18b9ae5b48e9" />

<img width="468" alt="image" src="https://github.com/user-attachments/assets/79c25fe5-aed0-4ed8-a37e-1a5218f7ae0c" />

<img width="468" alt="image" src="https://github.com/user-attachments/assets/35444f8c-9e05-4031-8044-ac39a67f32ce" />




