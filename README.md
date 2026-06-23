# Smart Environmental Monitoring & Alert System

## Project Overview

The Smart Environmental Monitoring & Alert System is an embedded solution designed to monitor critical environmental parameters in real time using the STM32 Nucleo-F103RB development board.

The system integrates multiple sensors to measure air quality, smoke concentration, temperature, and motion activity. Based on predefined threshold values, it generates visual and audible alerts while simultaneously displaying system status on an LCD module and transmitting sensor data to a Python-based dashboard through UART communication.

The project demonstrates the practical implementation of embedded systems, sensor interfacing, serial communication, real-time monitoring, and environmental safety applications.

---

## Problem Statement

Environmental hazards such as poor air quality, gas leakage, smoke generation, abnormal temperature conditions, and unauthorized motion often go undetected until they cause significant damage.

Most existing solutions are either expensive, cloud-dependent, or designed for monitoring a single parameter. This project aims to provide a low-cost, standalone, multi-sensor monitoring solution capable of real-time alert generation and visualization.

---

## Objectives

- Monitor air quality in real time.
- Detect smoke and harmful gases.
- Measure ambient temperature continuously.
- Detect human motion using PIR sensing.
- Generate multi-level alert notifications.
- Display live information locally on an LCD.
- Stream sensor data to a PC for visualization.
- Develop a complete embedded monitoring platform using STM32.

---

## System Architecture

### Input Sensors

- MQ-135 Air Quality Sensor
- MQ-2 Smoke and Gas Sensor
- DS18B20 Digital Temperature Sensor
- PIR Motion Sensor

### Processing Unit

- STM32 Nucleo-F103RB
- ARM Cortex-M3 Core
- 72 MHz Clock Frequency

### Output Devices

- 16×2 I2C LCD Display
- Green Status LED
- Yellow Warning LED
- Red Danger LED
- Active Buzzer
- Python Dashboard

---

## Hardware Components

| Component | Purpose |
|------------|------------|
| STM32 Nucleo-F103RB | Main Controller |
| MQ-135 | Air Quality Monitoring |
| MQ-2 | Smoke/Gas Detection |
| DS18B20 | Temperature Monitoring |
| PIR Sensor | Motion Detection |
| 16×2 LCD | Real-Time Display |
| Buzzer | Alert Generation |
| LEDs | Status Indication |
| Breadboard & Wires | Prototyping |

---

## Software Tools

- STM32CubeIDE
- STM32 HAL Libraries
- Embedded C
- Python
- PySerial
- Matplotlib

---

## Working Principle

The STM32 continuously acquires data from all connected sensors.

### Air Quality Monitoring

The MQ-135 sensor provides analog data corresponding to environmental air quality. The STM32 converts this signal using its internal ADC and categorizes the condition into:

- Good
- Warning
- Danger

### Smoke Detection

The MQ-2 sensor monitors smoke and gas levels. If the reading exceeds the defined threshold, the system immediately triggers emergency alerts.

### Temperature Monitoring

The DS18B20 sensor communicates using the 1-Wire protocol and provides accurate digital temperature measurements.

### Motion Detection

The PIR sensor detects changes in infrared radiation caused by human movement and generates motion alerts.

### Alert Logic

The system implements a three-level alert mechanism:

#### Normal Condition

- Green LED ON
- Buzzer OFF

#### Warning Condition

- Yellow LED ON
- Periodic buzzer indication

#### Danger Condition

- Red LED ON
- Continuous alarm buzzer

---

## Communication System

The STM32 transmits sensor data through UART at 115200 baud.

The transmitted data is processed by a Python application which generates a live monitoring dashboard using Matplotlib.

Example Data Format:

```text
28.5,1350,980,0,1
```

Where:

```text
Temperature, MQ135, MQ2, Smoke Flag, PIR Flag
```

---

## Key Features

- Multi-sensor integration
- Real-time monitoring
- Live LCD display
- UART communication
- Python dashboard visualization
- Three-tier alert mechanism
- Standalone operation
- Low-cost implementation
- No cloud dependency

---

## Applications

### Industrial Safety

Monitoring gas leaks and hazardous environmental conditions.

### Smart Buildings

Indoor air quality supervision and occupancy detection.

### Healthcare Facilities

Environmental monitoring in sensitive areas.

### Educational Laboratories

Embedded systems and sensor interfacing demonstrations.

### Smart Homes

Smoke detection and intrusion monitoring.

### Greenhouses

Temperature and environmental condition tracking.

---

## Results

The developed system successfully:

- Detected air quality variations.
- Identified smoke and gas conditions.
- Measured temperature accurately.
- Detected motion events.
- Generated visual and audible alerts.
- Displayed real-time data on LCD.
- Streamed live data to a Python dashboard.

The system operated reliably while maintaining a total project cost below ₹2000.

---

## Technical Concepts Demonstrated

- Embedded Systems Design
- STM32 Programming
- ADC Interfacing
- GPIO Programming
- UART Communication
- I2C Communication
- 1-Wire Communication
- Sensor Integration
- Real-Time Monitoring
- Data Visualization

---

## Future Enhancements

- ESP8266 / ESP32 Wi-Fi Integration
- Cloud Connectivity
- Mobile Application Support
- Historical Data Logging
- Machine Learning Based Anomaly Detection
- Custom PCB Development
- Commercial Product Deployment

---

## Authors

**Swapnil Saraswat**  
B.Tech Electronics & Communication Engineering  
Gati Shakti Vishwavidyalaya

**Amisha Singh**  
B.Tech Electronics & Communication Engineering  
Gati Shakti Vishwavidyalaya

**Ananya Kasaudhan**  
B.Tech Electronics & Communication Engineering  
Gati Shakti Vishwavidyalaya

**Pranjal Sharma**  
B.Tech Electronics & Communication Engineering  
Gati Shakti Vishwavidyalaya

---

## Project Documentation

The complete project presentation and supporting documentation are included in this repository.
