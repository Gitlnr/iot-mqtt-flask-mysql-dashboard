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
├── ROS2_Project/
│   └── src/
│       └── ROS2_Project_pkg/
│           ├── ROS2_Project_pkg/
│           │   ├── status_publisher.py
│           │   ├── command_listener.py
│           │   ├── robotarm_listener.py
│           │   ├── vehicle_listener.py
│           │   ├── flask_server.py
│           │   ├── __init__.py
│           │   └── templates/
│           │       └── index.html
│           │
│           └── setup.py
│
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

* ROS 2 nodes generate and publish data
* Topics transmit data between system components
* Services/actions handle control logic
* Vehicle System communicates with the Robot Arm
* Web interface visualizes data and sends commands
* Robot Arm executes the requested operations

---

## **V. How to Run**

1. Start ROS 2 environment

```
source /opt/ros/<distro>/setup.bash
```

2. Build workspace

```
colcon build
```

3. Run nodes

```
ros2 run <package_name> <node_name>
```

4. Launch full system

```
ros2 launch <package_name> <launch_file>.py
```

5. Open web interface

```
http://localhost:<port>
```

---

## **VI. Purpose**

This project helps in understanding:

* ROS 2 architecture (nodes, topics, services, actions)
* Real-time robotic communication
* System integration between multiple robotic components
* Full-stack robotics development (backend + interface)

---
