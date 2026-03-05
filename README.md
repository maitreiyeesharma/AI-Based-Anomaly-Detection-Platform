# 🏥 AI-Driven Healthcare Anomaly Detection System

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/maitreiyeesharma/AI-Based-Anomaly-Detection-Platform/blob/main/MedicalAnomaly_engineDashboard.ipynb)

![Build Status](https://img.shields.io/badge/build-passing-brightgreen)
![Python Version](https://img.shields.io/badge/python-3.10%2B-blue)
![License](https://img.shields.io/badge/license-MIT-green)

*(Optional: Place your recorded demo GIF of the dashboard here)*

## 📌 Project Overview
The **AI-Driven Healthcare Anomaly Detection System** is an end-to-end, real-time physiological monitoring platform. It bridges the gap between raw medical data ingestion and clinical decision support through automated anomaly detection and a centralized command dashboard. This project simulates an Intensive Care Unit (ICU) telemetry pipeline, designed to prevent alarm fatigue and provide immediate visual and acoustic alerts for critical patient states.

## 🏗️ System Architecture
The platform is built on a robust, multi-threaded pipeline:
1. **Data Ingestion Engine:** Acts as a virtual medical device, generating high-frequency streams of Heart Rate (Pulse) and Oxygen Saturation (SpO₂).
2. **Machine Learning Layer:** Utilizes an Isolation Forest and Keras Autoencoder ensemble to classify patient states as *Normal*, *Warning*, or *Critical* based on physiological thresholds.
3. **Persistence Layer:** Logs all telemetry and classification events into a local SQLite database for historical trending.
4. **Real-Time UI:** A Flask-based web interface utilizing Plotly for dual-axis, low-latency waveform monitoring.

## ⚙️ Core Features
* **Live Waveform Monitoring:** Real-time visual tracking with asynchronous UI reflows to ensure zero dashboard freezing.
* **Emergency Audio/Visual Alerts:** Synchronized Web Speech API notifications and CSS-pulsing highlights for critical events.
* **Resilient Threading:** Background processing queue that ensures the ML engine never blocks the data ingestion stream.

## 💻 Technology Stack
| Component | Technology Used | Purpose |
| :--- | :--- | :--- |
| **Frontend UI** | HTML/CSS, JS, Plotly | Real-time asynchronous data visualization |
| **Backend API** | Python, Flask, Threading | Non-blocking data routing and server management |
| **Database** | SQLite, SQLAlchemy ORM | High-speed local telemetry persistence |
| **Machine Learning** | Scikit-Learn, Keras | Unsupervised anomaly detection algorithms |

## 🚀 Quick Start
To experience the live simulated environment without local configuration:
1. Click the **Open in Colab** badge at the top of this repository.
2. Run the notebook execution cells sequentially.
3. Click the generated `localtunnel` / `ngrok` link to access the live Command HUD.
4. 
