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
