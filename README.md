# Face Recognition Based Attendance System  



This project takes the hassle out of attendance by using face recognition to mark attendance automatically. With Python, OpenCV, and dlib working behind the scenes, it captures video, recognizes familiar faces, and saves attendance details in an easy-to-use SQLite database. Managing and checking attendance is a breeze thanks to a straightforward Flask web interface.



---



## 📌 Overview  



This project blends computer vision technology with a simple web dashboard to make attendance seamless from start to finish. There are two main parts: the Face Registration process (where you add new faces to the system) and the Web Interface (where you can easily view and manage attendance records).

   - Extracts unique facial embeddings and saves them for recognition.  



2. **Web Interface (Flask + SQLite + HTML/CSS)**  

   - Displays attendance records in a simple, user-friendly dashboard.  

   - Stores data in a lightweight local database (SQLite).  



---



## ⚙️ System Architecture  



### 🔹 1. Face Registration Module  

**Technologies Used**  

- **OpenCV (`cv2`)** → Video capture & image preprocessing  

- **dlib** → Face detection, landmark extraction, and 128D face embeddings  

- **NumPy** → Feature vector storage and operations  



**Key Files**  

- `get_faces_from_camera_tkinter.py` → GUI application for capturing and registering faces  

- `features_extraction_to_csv.py` → Extracts and saves facial features into CSV format  



**Workflow**  

1. Capture frames from the webcam.  

2. Detect faces using dlib’s HOG-based face detector.  

3. Extract **68 facial landmarks**.  

4. Generate a **128D face descriptor** (unique digital identity).  

5. Save the images and feature vectors for recognition.  



---



### 🔹 2. Web Interface  

**Technologies Used**  

- **Flask** → Lightweight Python web framework  

- **SQLite** → File-based relational database for attendance records  

- **HTML/CSS/Bootstrap** → Frontend design and layout  



**Key Files**  

- `app.py` → Flask server for rendering pages and handling requests  

- `templates/index.html` → Web dashboard template  

- `attendance_taker.py` → Real-time face recognition and attendance marking  



**Workflow**  

1. Flask (`app.py`) serves the attendance dashboard.  

2. The database (`attendance.db`) stores name, date, and time of attendance.  

3. `attendance_taker.py` performs live recognition and inserts records into the database.  



---



## 🚀 Features  

Provides real-time face recognition and automatic attendance logging, with a user-friendly web dashboard for viewing daily or overall attendance. Easy local deployment with options to extend for larger datasets or future cloud deployment.  



