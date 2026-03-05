# AI-Based-Anomaly-Detection-Platform
"Real-time patient monitoring demo using simulated ML pipelines."

OPEN : Final_Project.ipynb File for main code and run it in colab or your Local Python Environment
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Maitreiyeesharma/AI-Based-Anomaly-Detection-Platform/blob/main/Final_Final_project%20(1).ipynb)

AI-Driven Healthcare Monitoring System
This notebook implements a real-time medical monitoring solution. It integrates machine learning for anomaly detection with a live Flask dashboard to visualize patient vitals and manage clinical alerts.

1. Environment and Infrastructure Setup
In this section, we install the necessary libraries for web serving (Flask), data persistence (SQLAlchemy), and machine learning (Scikit-learn, TensorFlow).

2. Database Model Definition
We define the relational schema for our system. The Patient model tracks user status, while VitalSigns stores historical telemetry data for heart rate and SpO2 levels.

3. Machine Learning Anomaly Detection Engine
This block initializes our ensemble ML approach. We generate synthetic 'Normal' baseline data to train an Isolation Forest and a Keras Autoencoder, allowing the system to identify deviations from healthy physiological patterns.

4. Real-time Streaming Simulation
To simulate a live hospital environment, we use a multi-threaded producer-consumer model. Sensor 'Producers' generate data streams, while 'Consumers' process the data through our ML engine and save it to the database.

5. Integrated Dashboard and UI Implementation
The final section launches the Flask web server. The UI features real-time Plotly charts with dual axes, audio alert triggers for critical states, and full control over patient monitoring sessions.

AI-Driven Healthcare Monitoring System: Technical Overview
This project implements an end-to-end real-time physiological monitoring platform. It is designed to bridge the gap between raw medical data ingestion and clinical decision support through automated anomaly detection and a centralized command dashboard.

Core System Architecture
Data Ingestion & Simulation: A multi-threaded engine acts as a virtual medical device, generating high-frequency streams of Heart Rate (Pulse) and Oxygen Saturation (SpO2). It includes a stochastic anomaly injector to simulate clinical emergencies.
ML Anomaly Engine: Vitals are passed through a classification pipeline that evaluates data against medical safety thresholds to categorize patient states as Normal, Warning, or Critical.
Persistence Layer: All telemetry and classification events are logged into a local SQLite database (medical_system.db) for historical trending and dashboard retrieval.
Real-Time Dashboard: A Flask-based web interface featuring:
Live Waveform Monitoring: Clean, dual-axis Plotly charts with transparent backgrounds for real-time visual tracking.
Patient Registry: Dynamic sidebar to manage active patient monitoring and status updates.
Emergency Controls: Manual 'Forced Alert' triggers for system testing and email notification verification.
Operational Instructions
To Start: Run the execution cell below. Click the provided Dashboard Ready proxy link.
Monitoring: Click '+ Add Patient' on the dashboard to initialize a new monitoring thread.
Alerts: The system will automatically trigger a 'Beep' audio cue if the selected patient enters a Warning or Critical state.
Maintenance: Use the 'Clear All Data' button to reset the database and terminate all active simulation threads.
Approch
Build a real-time healthcare monitoring system with an integrated ML anomaly detection engine and a Flask dashboard. This involves setting up a SQLite database at "/content/medical_system.db", training an ensemble model (Isolation Forest and Autoencoder) to detect vital sign irregularities, implementing a multi-threaded data stream simulation, and launching a web interface with Plotly visualizations and audio alerts for critical patient states.
