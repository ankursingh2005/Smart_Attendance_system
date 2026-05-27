# Smart Attendance System 📷📝

## Project Overview

This project is a Python-based **Smart Attendance System** that automates attendance tracking using **QR codes and a webcam**. The system scans QR codes in real time, records attendance automatically, prevents duplicate entries, and stores attendance records for future use.

The application reduces manual attendance efforts and provides a faster and more reliable attendance management solution.

---

## Features

- Reads and scans QR codes using webcam
- Real-time QR code detection and decoding
- Automatic attendance recording
- Prevents duplicate attendance entries
- Stores attendance data in a text file
- Fast and lightweight implementation
- Supports continuous scanning process
- Easy to modify and extend

---

## Project Structure

```text
Smart_Attendance_System
│
├── smart_attendance.py
├── attendance.txt
├── requirements.txt
└── README.md
```

---

## How to Run

### Step 1: Open terminal in project folder

Move to project directory:

```bash
cd Smart_Attendance_System
```

### Step 2: Install required libraries

```bash
pip install opencv-python pyzbar numpy
```

### Step 3: Run Python file

```bash
python smart_attendance.py
```

or

```bash
py smart_attendance.py
```

---

## Working Process

1. Webcam captures live video feed.
2. QR codes are detected using Pyzbar.
3. QR code data is decoded.
4. The system checks whether attendance already exists.
5. If unique:
   - Attendance is saved
6. If already present:
   - Duplicate entry is ignored

---

## Input Format

QR Code Example:

```text
Ankur Singh
```

or

```text
Student_ID_101
```

---

## Output Format

Attendance file (`attendance.txt`) generated automatically:

```text
Ankur Singh
Rahul Kumar
Aman Verma
```

---

## Logic Used

Duplicate Check:

```python
if name not in attendance_list:
    attendance_list.append(name)
```

This ensures each person is marked only once during a session.

---

## Assumptions Made

Some conditions were not explicitly defined, so the following assumptions were used:

1. Each QR code contains unique student information.

2. Duplicate attendance within the same session is ignored.

3. Attendance is stored in a text file.

4. Webcam remains active until user stops the program.

5. QR codes are clearly visible to the camera.

6. Attendance follows the order in which QR codes are scanned.

---

## Technologies Used

- Python
- OpenCV
- Pyzbar
- NumPy

---

## Future Improvements

- Add GUI for better user experience
- Integrate MySQL/SQLite database
- Add Face Recognition authentication
- Support multiple camera inputs
- Generate attendance reports automatically
- Add email or SMS notifications
- Integrate cloud storage

---

## Author

**Ankur Singh   & Anjali Singh**  
B.Tech CSE 

```
