📖 Project Overview
SmartShelf is an end-to-end IoT and Machine Learning platform designed to mitigate post-harvest crop loss through predictive analytics. By strictly monitoring the micro-climate of storage facilities, this system detects the early onset of spoilage before it becomes visible to the human eye.

The solution bridges the gap between hardware and software, utilizing a network of environmental sensors to feed real-time data into a trained Machine Learning model. This model analyzes patterns in temperature, humidity, and gas emissions to predict spoilage probability, which is then visualized on a responsive web dashboard for actionable insights.

🏗️ System Architecture
This project follows a Sensor-to-Insight data pipeline:

Data Acquisition Layer (IoT Edge):

Custom-built IoT nodes equipped with precision sensors (Temperature, Humidity, VOC/Gas) continuously monitor the storage environment.

Communication & Transport:

Data is transmitted securely to the cloud server via MQTT/HTTP protocols over Wi-Fi.

Intelligence Layer (ML Engine):

The backend receives the time-series data and feeds it into a pre-trained Machine Learning model (Random Forest regressor).

The model evaluates the environmental parameters against known spoilage thresholds to classify the current status (e.g., Safe, Warning, Critical).

Application Layer (Web Interface):

A full-stack web application serves the results. It features a real-time dashboard displaying sensor readings, historical trends, and ML-generated alerts.

Server Layer (Backend):

A local flask server which fetches sensor data from a remote ThinkSpeak server and pridict the spoilage using the RandomForest regressor

🛠️ Tech Stack
Hardware (IoT)
Microcontroller: [ESP32]

Sensors: [DHT11 (Temp/Hum), MQ-135(CO2), MQ-2(Methane)

Connectivity: GSM Module

Software & Backend
Programming Language: Python (ML/Backend), C++ (Firmware)

ML Frameworks: Scikit-learn

Backend Framework: Flask ser

Database: Firebase / MongoDB / PostgreSQL

Frontend
Framework: React.js / HTML5, CSS3, JavaScript

Visualization: Chart.js / D3.js (for real-time graphing)

🌟 Key Features
Real-Time Monitoring: Live tracking of storage silo/warehouse conditions with low latency.

Predictive Spoilage Detection: ML algorithms analyze environmental trends to forecast potential spoilage events hours or days in advance.

Automated Alerts: (Optional) Notification system via Email/SMS when the ML model detects a "Critical" status.

Data Visualization: Interactive graphs showing temperature and humidity fluctuations over time.

Scalable Architecture: Designed to handle data from multiple sensor nodes across different storage units.
