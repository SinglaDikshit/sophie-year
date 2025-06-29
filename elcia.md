# Pulse Track: AI-Enhanced Multi-Modal Vitals Monitoring System

## Hackathon Proposal for ELCIA Tech Summit 2025

### 1. Team Details
**Team Name:** Hardweared 
**Institution:** IIT Bombay
**Team Members:**  
- Dikshit Singla - Team Lead
- dikshit131105@gmail.com
- Ravindra Naga - Hardware Integration Specialist
- email
- Ankur Gupta - Software & Testing Engineer
- email

**Contact:** 8699300395

### 2. Project Title
**Pulse Track: AI-Enhanced Multi-Modal Vitals Monitoring System with Edge Intelligence**

### 3. Target Application Area
**Remote Patient Monitoring – Comprehensive Vitals Analysis with Predictive Health Analytics**

### 4. Overview of Proposed Solution

Our solution addresses the critical need for continuous, accurate, and intelligent health monitoring in remote settings. The system combines photoplethysmography (PPG), temperature sensing, and motion detection with advanced AI/ML algorithms running on edge computing platforms.

**Problem Addressed:** Traditional vitals monitoring systems suffer from motion artifacts, inconsistent readings, and lack of predictive capabilities. Healthcare providers need real-time, accurate vitals data with early warning systems for patients with cardiovascular conditions, respiratory issues, or post-operative recovery.

**Innovation Highlights:**
- **Edge AI Implementation:** TinyML models running on ESP32 for real-time signal processing
- **Multi-sensor Fusion:** Advanced algorithms combining PPG, temperature, and IMU data for artifact reduction
- **Predictive Analytics:** Early detection of arrhythmias, hypoxemia, and cardiovascular anomalies
- **Adaptive Learning:** Personalized baselines that adapt to individual physiological patterns

### 5. Sensors and Compute Board

| Component Type | Part Name/Number | Estimated Cost (INR) | Purpose |
|---|---|---|---|
| PPG/SpO2 Sensor | MAX30102 | 320 | Heart rate, SpO2 monitoring |
| Non-contact Temperature | MLX90614 | 1000 | Body temperature measurement |
| IMU/Accelerometer | ADXL335 | 1280 | Motion detection, artifact removal |
| Microcontroller | ESP32-WROOM-32 | 800 | Edge AI processing, WiFi connectivity |
| Display | 0.96" OLED SSD1306 | 200 | Real-time data visualization |
| Power Management | LiPo Battery + Charging | 300 | Portable operation |
| Miscellaneous | PCB, Resistors, Capacitors | 100 | Circuit implementation |
| **Total Cost** | | **4000** | **Within Budget** |

### 6. Circuit Connection & Pinout Table

| Sensor/Module | ESP32 Pin | Function | Protocol |
|---|---|---|---|
| MAX30102 SDA | GPIO 21 | I2C Data | I2C |
| MAX30102 SCL | GPIO 22 | I2C Clock | I2C |
| MAX30102 INT | GPIO 4 | Interrupt | Digital |
| MLX90614 SDA | GPIO 21 | I2C Data (shared) | I2C |
| MLX90614 SCL | GPIO 22 | I2C Clock (shared) | I2C |
| ADXL335 X-axis | GPIO 36 (ADC) | X-axis motion | Analog |
| ADXL335 Y-axis | GPIO 39 (ADC) | Y-axis motion | Analog |
| ADXL335 Z-axis | GPIO 34 (ADC) | Z-axis motion | Analog |
| OLED SDA | GPIO 21 | Display Data | I2C |
| OLED SCL | GPIO 22 | Display Clock | I2C |

### 7. Testing Plan (TRL-8 Readiness)

• **Accuracy Validation:** Compare heart rate measurements against commercial pulse oximeters (±3 BPM accuracy target)
• **Motion Artifact Testing:** Validate signal quality during various activities (walking, typing, resting)
• **Temperature Calibration:** Cross-validation with medical-grade thermometers (±0.3°C accuracy)
• **24-Hour Continuous Operation:** Battery life and data consistency testing with 99% uptime target
• **Environmental Testing:** Temperature drift analysis (-10°C to 50°C), humidity resistance testing
• **AI Model Validation:** Arrhythmia detection accuracy testing with synthetic and real ECG data
• **Field Testing:** 48-hour real-world deployment with multiple subjects for system validation

### 8. Indian Sensor Substitution Plan

**Current Strategy:** Design modular sensor interfaces with standardized I2C/SPI protocols
**Future Adaptation:** 
- Implement software abstraction layers for easy sensor swapping
- Develop calibration algorithms adaptable to different sensor characteristics
- Create open-source hardware design compatible with Indian sensor form factors
- Establish partnerships with emerging Indian sensor manufacturers
- Maintain backward compatibility through firmware updates

### 9. Expected Output

**Real-time Visualizations:**
- Live PPG waveform display with heart rate and SpO2 values
- Temperature trending with fever alerts
- Motion activity levels and posture detection
- AI-generated health scores and risk assessments

**Data Logging:**
- Timestamped sensor data stored locally and cloud-synchronized
- Statistical analysis reports (daily/weekly/monthly trends)
- Anomaly detection logs with severity classification

**Alert System:**
- Immediate alerts for critical values (HR >100/<60, SpO2 <90%, Fever >38°C)
- Predictive warnings for potential health deterioration
- Emergency contact notifications via SMS/email

### 10. AI/ML Innovation Components

**Edge AI Architecture:**
- **TensorFlow Lite Micro:** Optimized neural networks for real-time processing
- **Signal Processing:** FFT-based noise reduction and artifact elimination
- **Fusion Algorithms:** Kalman filtering for multi-sensor data integration
- **Anomaly Detection:** Isolation Forest algorithms for outlier identification
- **Predictive Modeling:** LSTM networks for trend analysis and early warning

**Machine Learning Features:**
- **Personalized Baselines:** Adaptive learning of individual physiological patterns
- **Motion Compensation:** AI-driven artifact removal using IMU data correlation
- **Context Awareness:** Activity recognition to adjust measurement sensitivity
- **Health Scoring:** Multi-parameter risk assessment algorithms

### 13. Declaration

We understand and agree to comply with cost constraints (under ₹4,000), TRL-8 readiness goals, comprehensive testing requirements, and technology sharing policies. Our team commits to open-source hardware design and collaborative development approach to support the Indian electronics ecosystem.

**Signatures:**
[Team Member Signatures]

---

**Contact Information:**
Email: [email]  
Phone: [phone]  
Institution: [institution address]
