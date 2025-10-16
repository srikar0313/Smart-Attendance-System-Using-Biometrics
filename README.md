# Smart Attendance System Using Biometrics

A Python-based attendance management system that uses **face recognition (biometrics)** to record and manage attendance automatically.

---

## 📖 Table of Contents

1. [Overview](#overview)
2. [Features](#features)
3. [Architecture & Workflow](#architecture--workflow)
4. [Project Structure](#project-structure)
5. [Installation & Setup](#installation--setup)
6. [Usage](#usage)
7. [Screenshots / Demo](#screenshots--demo)
8. [Limitations & Future Work](#limitations--future-work)
9. [Credits & References](#credits--references)
10. [License](#license)

---

## 🧩 Overview

This application enables automated attendance taking using **facial biometrics**.  
Instead of manual roll calls or ID card swipes, users’ faces are recognized and their attendance is recorded in an Excel sheet or database.  
It’s designed for schools, colleges, and workplaces where contactless attendance is desired.

**Key idea:**
- Capture face using a webcam
- Match it against stored profiles
- Mark attendance automatically
- Display results via an intuitive GUI

---

## ⚙️ Features

- Real-time **face detection & recognition**
- **GUI interface** for user/admin interaction
- Uses pretrained **dlib ResNet model**
- Stores attendance logs (Excel / CSV)
- Option to add new users dynamically
- Simple, offline, and lightweight

---

## 🧠 Architecture & Workflow

1. **Camera input:** captures live face frames  
2. **Face detection:** locates and extracts face region  
3. **Embedding generation:** generates 128-D facial features using pretrained model  
4. **Comparison:** compares live face to stored faces  
5. **Logging:** records user name, ID, timestamp in attendance file  
6. **Interface:** displays results and allows viewing / exporting attendance logs

---

## 📁 Project Structure
Smart-Attendance-System-Using-Biometrics/
│
├── app.py
├── main.py
├── ui_design.py
├── dlib_face_recognition_resnet_model_v1.dat
├── *.jpeg # UI screenshots, sample outputs
└── README.md # ← You are here

| File | Description |
|------|--------------|
| **app.py** | Entry point; initializes app and connects logic to GUI |
| **main.py** | Core logic for face recognition and attendance recording |
| **ui_design.py** | Defines layout, buttons, and user interface |
| **dlib_face_recognition_resnet_model_v1.dat** | Pretrained deep learning model for face embeddings |
| **.jpeg files** | Screenshots and sample outputs |

---

## 🧩 Installation & Setup

### 1️⃣ Prerequisites
- Python **3.7+**
- A working **webcam**
- (Recommended) A **virtual environment**

### 2️⃣ Clone Repository
```bash
git clone https://github.com/srikar0313/Smart-Attendance-System-Using-Biometrics.git
cd Smart-Attendance-System-Using-Biometrics
3️⃣ Install Dependencies

If a requirements.txt file isn’t present, manually install these:
pip install dlib opencv-python numpy pandas
Note: Installing dlib requires CMake and developer tools.
On Ubuntu:
sudo apt-get install cmake libboost-all-dev
On Windows: install Visual Studio Build Tools (C++).

4️⃣ Run the App
python app.py
```
🚀 Usage

Launch the program — GUI opens automatically.

The webcam turns on and starts detecting faces.

If your face matches an existing profile, attendance is recorded.

Admin can:

View attendance logs

Export them to Excel / CSV

Add new users by capturing their face

🖼️ Screenshots / Demo

Sample UI & output files are included in the repository (.jpeg images).
You can embed them here, for example:




🧩 Limitations & Future Work
Current Limitation	Possible Improvement
Works on single camera	Add multi-camera / network support
No liveness detection	Add anti-spoofing (blink detection, 3D depth)
Accuracy drops in poor lighting	Improve preprocessing or use infrared sensors
Local-only	Deploy backend + cloud storage
Manual registration	Enable auto-registration via admin panel
🙌 Credits & References

Author: Srikar0313

Model: dlib_face_recognition_resnet_model_v1.dat

Libraries Used:

dlib

opencv-python

numpy, pandas

tkinter / PyQt (depending on UI design)
