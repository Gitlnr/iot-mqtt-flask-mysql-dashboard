## **I. Overview**
This is a simple full-stack IoT project built to understand how the MQTT protocol works.
The system simulates:
* Temperature data generation
* Real-time data transfer using MQTT
* Data storage in MySQL
* Web-based monitoring and control using Flask
---
## **II. Project Structure**

```
IOT_PROJECT/
│
├── templates/
│   └── index.html
├── app.py
├── mqtt_to_mysql.py
├── device_sim.py
├── sql_database.sql
└── README.md
```
---
## **III. Components**

### 1. Publisher
* Generates random temperature values
* Sends data every 5 seconds using MQTT

### 2. MQTT Broker
* Acts as a communication bridge
* Transfers messages between publisher and subscribers

### 3. Subscriber
* Receives temperature data
* Stores it in MySQL database

### 4. Device Simulator
* Listens for ON/OFF commands
* Simulates a device response

### 5. Flask Web App
* Displays temperature data in graph
* Provides ON/OFF control buttons

### 6. MySQL Database
* Stores temperature data with timestamps

---

## **IV. Workflow**

1. Publisher sends temperature data
2. MQTT broker forwards it
3. Subscriber stores data in MySQL
4. Flask app fetches and displays data
5. User sends ON/OFF commands
6. Device simulator executes command

---

## **V. How to Run**

1. Start MQTT broker (Mosquitto)

2. Run publisher:
   python publisher.py

3. Run subscriber:
   python mqtt_to_mysql.py

4. Run device simulator:
   python device_sim.py

5. Run Flask app:
   python app.py

6. Open browser:
   http://localhost:5000

---

## **VI. Purpose**

This project helps in understanding:
* MQTT publish/subscribe model
* Real-time IoT communication
* Backend + database integration
* Basic web dashboard for IoT

---

## **VII. Future Improvements**

* Add real sensors
* Deploy on cloud
* Add authentication
* Improve UI dashboard

---
