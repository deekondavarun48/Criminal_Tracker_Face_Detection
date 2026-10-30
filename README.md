# 🔍 Criminal Tracker & Face Detection System 👤⚡

A web-based intelligent law enforcement and criminal tracking platform built with **Django**, **DeepFace**, **TensorFlow**, and **OpenCV**. The system enables administrative personnel and law enforcement officers to manage crime logs, track criminal records, register precinct stations, and perform biometric facial recognition against verified database records.

---

## 🌐 Live Demonstration

* **Production URL:** [https://criminal-tracker-face-detection.onrender.com](https://criminal-tracker-face-detection.onrender.com)
* **Status:** Operational (Render Web Service)

---

## 📌 Key Features

* **Biometric Face Verification:** Utilizes deep learning facial recognition pipelines (`DeepFace`, `MTCNN`, `RetinaFace`, and `TensorFlow`) to match suspect facial inputs against enrolled criminal mugshots.
* **Law Enforcement Administration:**
  * Add, modify, and manage police department precincts and stations.
  * Register, assign, and manage law enforcement officer profiles with secure authentication credentials.
* **Criminal Record & Crime Incident Management:**
  * Catalog criminal identities with national identity markers (Aadhaar), biometric images, contact details, and demographic metadata.
  * Log and trace incidents, crime types, dates, and related forensic descriptions.
* **Role-Based Portals:**
  * **Admin Portal:** Central system monitoring, police department oversight, and database operations.
  * **Officer / User Portal:** Incident searching, suspect record lookups, and facial verification queries.
* **Production-Hardened Architecture:** Optimized for headless Linux environments using SQLite database storage and headless computer vision runtimes.

---

## 🛠️ Technology Stack

| Component | Technology / Library |
| :--- | :--- |
| **Backend Framework** | Django 4.1.x (Python 3.10) |
| **Deep Learning & CV** | TensorFlow 2.11, DeepFace, OpenCV (`opencv-python-headless`), RetinaFace, MTCNN |
| **Database** | SQLite3 |
| **Frontend Templates** | Django Templating Engine, HTML5, CSS3, Bootstrap |
| **Deployment Platform** | Render Cloud Application Platform |

---

## 📂 Project Architecture

```text
Criminal_Tracker_Face_Detection/
├── Criminal_Tracker_Face_Detection/    # Core Django project configuration
│   ├── __init__.py
│   ├── asgi.py
│   ├── settings.py                    # Database, hosts, and static configurations
│   ├── urls.py                        # Central routing table
│   └── wsgi.py                        # WSGI entrypoint
├── adminapp/                          # Admin portal and records management logic
│   ├── migrations/
│   ├── models.py                      # Crime, Criminal, Station, and Officer schemas
│   └── views.py
├── homeapp/                           # Public landing pages and shared view handling
│   └── views.py
├── userapp/                           # Officer portal and face validation modules
│   └── views.py
├── assets/                            # Static design assets and templates
│   ├── static/
│   └── templates/
├── media/                             # Uploaded mugshots and profile imagery
├── manage.py                          # Django execution CLI
└── requirments.txt                    # Project dependencies
