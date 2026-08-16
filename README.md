# 🛡️ Sentinel – Behavioral Biometrics-Based Intrusion Detection System

> An advanced continuous authentication and intrusion detection system leveraging Keystroke Dynamics to verify user identity in real-time, moving beyond traditional static passwords.

---

## 📌 Overview

Sentinel is a cybersecurity graduation project designed to establish a continuous authentication layer. Traditional passwords only authenticate the "secret" rather than the "user", leaving systems vulnerable if credentials are compromised. 

Sentinel continuously monitors keyboard typing characteristics (such as hold times and flight latencies) to detect unauthorized access, featuring real-time anomaly detection, behavioral user profiling, and an interactive dashboard.

---

## 🏗️ System Architecture

```text
+-------------------------------------------------------------------------+
|                        FRONTEND / CLIENT INTERFACE                      |
|           (Keystroke Data Capture & Live Behavioral Inference)          |
+-------------------------------------------------------------------------+
                                     |
                                     v
+-------------------------------------------------------------------------+
|                            FLASK BACKEND SERVER                         |
|      (Scaled-Manhattan Detection Engine, User Modeling, REST APIs)      |
+-------------------------------------------------------------------------+
            |                                           |
            v                                           v
+-----------------------+                   +-----------------------------+
|    SQLITE DATABASE    |                   |     STREAMLIT DASHBOARD     |
| (Templates & Profiles)|                   | (Live Feed & Visualizations)|
+-----------------------+                   +-----------------------------+
✨ Features
 Continuous Authentication: Moves past one-time logins to verify user identity continuously throughout the session.
 Behavioral Biometrics: Analyzes unique typing rhythms, dwell times, and flight times.
 Optimized Detection Engine: Powered by the Scaled-Manhattan Detector, chosen after evaluating 14 distinct machine learning and statistical models.  
 High Accuracy: Achieved an Equal Error Rate (EER) of 9.61% against the benchmark CMU Keystroke Dynamics dataset.  
 Two-Mode Separation: Decouples offline dataset training pipelines from live browser-based inference environments to resolve microsecond versus millisecond timing discrepancies.  
📊 Dashboard & Interface
Live Analysis Feed
Behavioral Statistics & Risk Metrics
🛠️ Tech Stack
 Backend: Python, Flask  
 Frontend: HTML, CSS, JavaScript (Keystroke Event Listeners)
 Database: SQLite  
 Data Science & ML: Scaled-Manhattan Detector, Statistical Analysis Frameworks
 Dashboard / Visualization: Streamlit / Web UI
🚀 Installation & Setup
1. Clone the Repository
git clone [https://github.com/Rer-cys/Sentinel.git](https://github.com/Rer-cys/Sentinel.git)
cd Sentinel
2. Create Virtual Environment
python -m venv .venv
Windows:
.venv\Scripts\activate
macOS / Linux:
source .venv/bin/activate
3. Install Dependencies
pip install -r requirements.txt
4. Run the Server
python server.py
📁 Project Structure
Sentinel/
│
├── server.py             # Flask backend & detection logic
├── database.py           # SQLite database management
├── model.py              # Scaled-Manhattan algorithm implementation
├── requirements.txt      # Project dependencies
├── static/               # CSS, JavaScript, and assets
└── templates/            # HTML user interfaces
👥 Project Team
 Remas Hadi Al-Qahtani (University of Bisha - College of Computers and Information Technology)
 Team Members: Layla Alqahtani, Razan Alqahtani, Hanan Alqahtani, Rema Alharthi, Layla Jabar

  Supervisor: Dr. Mokhtar Ghaleb 
📜 License
This project is developed as an academic graduation project for the University of Bisha.
