
#  EV Dashboard System

#  Project Overview

The "EV Dashboard System" is an embedded system project designed to monitor and display important electric vehicle parameters in real time. The system uses an "STM32F103C8T6 microcontroller" to process vehicle inputs and sensor data.

Four potentiometers are used to simulate the "acceleration pedal, brake pedal, battery State of Charge (SOC), and motor temperature". Three "HC-SR04 ultrasonic sensors" are used to detect obstacles at the front, left, and right sides of the vehicle.

The processed data is communicated to a "Python Dashboard through UART", providing a user-friendly interface for monitoring vehicle status and obstacle detection.


# Objectives

- To develop an embedded EV Dashboard system using STM32.
- To monitor important EV parameters in real time.
- To simulate accelerator and brake pedal inputs.
- To monitor battery SOC and motor temperature.
- To detect obstacles using ultrasonic sensors.
- To transmit vehicle data using UART communication.
- To display vehicle information through a Python Dashboard.
- To test and validate the system using PICSimLab.



# Features

-  Acceleration Pedal Monitoring
-  Brake Pedal Monitoring
-  Battery State of Charge (SOC) Monitoring
-  Motor Temperature Monitoring
-  Front Obstacle Detection
-  Left Obstacle Detection
-  Right Obstacle Detection
-  Real-Time Vehicle Parameter Display
-  Obstacle Warning System
-  UART Communication
-  Python Dashboard Interface
-  PICSimLab Simulation


# System Architecture


                 +----------------------+
                 |     User Inputs      |
                 |  4 Potentiometers    |
                 | Accelerator / Brake  |
                 | SOC / Motor Temp.    |
                 +----------+-----------+
                            |
                            v
                 +----------------------+
                 |   STM32F103C8T6      |
                 |    Microcontroller    |
                 +----------+-----------+
                            |
              +-------------+-------------+
              |                           |
              v                           v
     +----------------+          +------------------+
     | EV Dashboard   |          |  ADAS / Obstacle |
     | Control        |          |  Detection       |
     +----------------+          +--------+---------+
                                           |
                         +-----------------+-----------------+
                         |                 |                 |
                         v                 v                 v
                    Front HC-SR04     Left HC-SR04     Right HC-SR04
                         Ultrasonic Sensors
                                           |
                                           v
                                  +----------------+
                                  | UART Communication |
                                  +--------+-------+
                                           |
                                           v
                                  +----------------+
                                  | Python Dashboard |
                                  +----------------+
                                  | Component               | Purpose                                                  |
# Hardware Components
| STM32F103C8T6            Main microcontroller                                     
| Potentiometer × 4        Simulates accelerator, brake, SOC, and motor temperature 
| HC-SR04 × 3              Front, left, and right obstacle detection                
| LEDs                     Status and warning indications                          
| Push Buttons / Switches  User inputs and control functions    

# Software and Tools
Embedded C – For firmware development
STM32CubeIDE – For coding, building, and debugging
STM32CubeMX – For microcontroller and peripheral configuration
HAL Drivers – For STM32 peripheral interfacing
PICSimLab – For simulation and testing
Python – For dashboard development
UART – For communication between STM32 and Python Dashboard

# Working Principle
The STM32F103C8T6 microcontroller initializes the required peripherals.
Four potentiometers provide analog inputs for:
Acceleration Pedal
Brake Pedal
Battery SOC
Motor Temperature

The STM32 reads and processes these analog values using the ADC.
Three HC-SR04 ultrasonic sensors measure obstacles from the:
Front
Left
Right
The microcontroller processes the sensor data and determines the vehicle status.
The processed information is transmitted to the Python Dashboard using UART communication.
The Python Dashboard displays the vehicle parameters and obstacle detection information in real time.
Warning indicators are activated when an obstacle is detected within the defined range.
The complete system is continuously monitored and tested using PICSimLab.

# Vehicle Parameters

The system monitors the following parameters:

Accelerator Pedal:The potentiometer simulates the accelerator pedal input and is used to control the vehicle speed.

Brake Pedal:The potentiometer simulates the brake pedal input and represents the braking condition of the vehicle.

Battery SOC:The potentiometer represents the battery State of Charge and helps monitor the available battery level.

Motor Temperature:The potentiometer simulates motor temperature and helps monitor the motor's operating condition.

Obstacle Detection:Three HC-SR04 ultrasonic sensors are used for obstacle detection.
Front Sensor – Detects obstacles in front of the vehicle.
Left Sensor – Detects obstacles on the left side.
Right Sensor – Detects obstacles on the right side.

The sensor data is processed by the STM32 and displayed on the Python Dashboard.

Communication:The system uses UART communication to transfer the processed data from the STM32F103C8T6 microcontroller to the Python Dashboard.

STM32 Microcontroller
        |
        | UART
        v
Python Dashboard
        |
        v
Real-Time Vehicle Monitoring

Simulation:The project is simulated and tested using PICSimLab.

The simulation verifies:

Potentiometer inputs
Vehicle parameter monitoring
Ultrasonic sensor-based obstacle detection
Dashboard indicators
UART data communication
Real-time dashboard updates
📸 Project Demo

# Project Structure
EV-Dashboard/
│
├── Core/
│   ├── Inc/
│   └── Src/
│
├── Drivers/
│
├── Python-Dashboard/
│
├── Simulation/
│
├── Documentation/
│
├── Images/
│
├── README.md
│
└── .gitignore

# Future Enhancements
CAN communication for real vehicle applications
IoT-based remote vehicle monitoring
Mobile application integration
GPS-based vehicle tracking
Advanced battery health monitoring
Automatic emergency alerts
Cloud-based data logging
Advanced ADAS features

Author Name
Laxmi Shekayi 
ECE branch 
