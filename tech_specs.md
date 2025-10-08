<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" style="height:64px;margin-right:32px"/>

# imu and gnss are not together but different

gnss : [https://github.com/YahboomTechnology/GPS_Module](https://github.com/YahboomTechnology/GPS_Module)

Thank you for the clarification. You're correct that the IMU and GNSS are separate components. Let me provide the corrected details in Markdown format:

## RoboSense Helios 16 Channel LiDAR

### General Information

- **Component Name:** Helios 16
- **Manufacturer/Model:** RoboSense / Helios 16
- **Category:** 3D LiDAR Sensor (Automotive Grade)[^1]


### Technical Specifications

| Parameter | Value |
| :-- | :-- |
| Number of Channels | 16 |
| Laser Wavelength | 905 nm |
| Laser Safety Level | Class 1 Eye-Safe |
| Measurement Range | 0.2 m to 150 m (110 m @10% NIST) |
| Blind Zone | 0.2 m |
| Accuracy (Typical) | 1 cm (1σ) / 3 cm (3σ) |
| Horizontal FOV | 360° |
| Horizontal Angle Resolution | 0.1° / 0.2° / 0.4° |
| Frame Rate | 5 Hz / 10 Hz / 20 Hz |
| Rotation Speed | 300 / 600 / 1200 rpm |
| Vertical FOV | 30° (-15° ~ +15°) |
| Vertical Angle Resolution | Uniform 2° |
| Point Cloud Output | 288,000 pts/s (single return), 576,000 pts/s (dual return) |
| Operating Voltage | 9V ~ 32V |
| Power Consumption | 12W (Typical) |
| Dimensions | Diameter 100 mm × Height 100 mm |
| Weight | 1000g ± 50g |
| Operating Temperature | -40°C ~ +60°C |
| Protection Level | IP67 / IP6K9K |

### Connectivity and Data Output

- **Ethernet Output:** 100 Base-T1
- **Data Protocol:** UDP packets over Ethernet
- **Data Contents:** 3D spatial coordinates, reflection intensity, timestamps
- **Time Synchronization:** GPS, PTP \& gPTP[^1]


### Software Integration

- **Supported SDKs/APIs:** RoboSense SDK, ROS drivers
- **Operating Systems:** Linux, Windows
- **Compatible Frameworks:** ROS ecosystem, NVIDIA Jetson AGX Orin[^1]


## Yahboom GNSS Module (Separate Component)

### General Information

- **Component Name:** Yahboom GPS Module
- **Manufacturer/Model:** Yahboom / ATGM336H-5N based
- **Category:** GNSS Positioning Module


### Technical Specifications

| Parameter | Value |
| :-- | :-- |
| Supported Systems | BDS (China), GPS (USA), GLONASS (Russia), QZSS (Japan) |
| Antenna Circuit | π-type antenna circuit |
| Impedance Matching | 50Ω |
| Standing Wave Ratio | <1.6 |
| Positioning Accuracy | 2.5 meters (CEP50) |
| Tracking Sensitivity | -162dBm |
| Interfaces | Type-C and USB |

### Software Integration

- **Compatible Platforms:** Computer, Raspberry Pi, Jetson
- **Software Support:** ROS-related tutorials and source codes
- **Programming Language:** C++


## Yahboom 10-Axis IMU (Separate Component)

### General Information

- **Component Name:** 10 Axis IMU
- **Manufacturer/Model:** Yahboom / IMU 10-Axis Inertial Navigation Sensor Module
- **Category:** Inertial Measurement Unit (IMU)[^1]


### Communication Specifications

| Parameter | Value |
| :-- | :-- |
| Serial Communication | Default 9600 bps (4800-921600 bps selectable) |
| I2C Interface | Hardware I2C up to 400KHz, Software I2C up to 100KHz |
| Output Rate | Default 10Hz (0.2Hz-200Hz selectable) |
| Startup Time | 1000ms |
| Operating Voltage | 5V or 3.3V |
| Operating Current | 12mV |
| Dormant Current | 15μA |

### Sensor Performance

| Sensor Type | Parameter | Value |
| :-- | :-- | :-- |
| **Accelerometer** | Measuring Range | ±16g |
|  | Resolution | 0.0005 g/LSB |
|  | RMS Noise | 0.75-1mg-rms |
|  | Static Zero Drift | ±20-40mg |
| **Gyroscope** | Measuring Range | ±2000°/s |
|  | Resolution | 0.061 (°/s)/LSB |
|  | RMS Noise | 0.028-0.07 (°/s)-rms |
|  | Static Zero Drift | ±0.5-1°/s |
| **Magnetometer** | Measuring Range | ±2 Gauss |
|  | Resolution | 0.0667 mGauss/LSB |
| **Barometer** | Measuring Range | 300-1100 hPa |
|  | Resolution | 0.5 Pa-RMS |
|  | Relative Accuracy | ±0.06 hPa |

### Angle Measurement

- **Pitch/Roll Range:** X: ±180°, Y: ±90°
- **Yaw Range:** Z: ±180°
- **Inclination Accuracy:** 0.1° (Static), 0.5° (Dynamic)
- **Yaw Accuracy:** 1° (without magnetic interference), 0.5° (dynamic)[^1]


### Physical Specifications

- **Dimensions (without case):** 43.1mm × 31.5mm
- **Dimensions (with metal case):** 46mm × 60mm × 11.7mm
- **Weight (without case):** 6.4g
- **Weight (with metal case):** 54.4g
- **Operating Temperature:** -40°C to +85°C
- **Impact Resistance:** 20kg (bare board)[^1]


### Output Content

- On-chip time
- 3-axis acceleration
- 3-axis angular velocity
- 3-axis magnetic field
- 3-axis angle
- Quaternion
- Port state
- Air pressure
- Altitude[^1]


### External Auxiliary

- **D1 port** can be connected to GPS module to form inertial navigation unit[^1]


### Software Integration

- **Operating Systems:** Bare-metal, Arduino, Raspberry Pi, Linux
- **Compatible Frameworks:** Arduino IDE, Python (PySerial), ROS[^1]


## Intel® RealSense™ Depth Camera D435i

### General Information

- **Component Name:** Intel® RealSense™ Depth Camera D435i
- **Manufacturer/Model:** Intel / D435i
- **Category:** Depth Sensing Camera (with IMU)[^1]


### Technical Specifications

| Parameter | Value |
| :-- | :-- |
| Use Environment | Indoor/Outdoor |
| Image Sensor Technology | Global Shutter |
| Ideal Range | 3m to 3m |
| Depth Technology | Stereoscopic |
| Minimum Depth Distance | ~28 cm |
| Depth Accuracy | <2% at 2m |
| Depth Field of View | 87° × 58° |
| Depth Stream Resolution | Up to 1280 × 720 |
| Depth Stream Frame Rate | Up to 90 fps |
| RGB Frame Resolution | 1920 × 1080 |
| RGB Frame Rate | 30 fps |
| RGB Sensor Technology | Rolling Shutter |
| RGB Sensor FOV | 69° × 42° |
| RGB Sensor Resolution | 2 MP |
| Camera Dimensions | 90 mm × 25 mm × 25 mm |
| Connectors | USB-C 3.1 Gen 1 |

### Software Integration

- **Supported SDKs/APIs:** Intel RealSense SDK 2.0 (Librealsense)
- **Operating Systems:** Windows 10, Ubuntu 18.04/20.04
- **Compatible Frameworks:** ROS1/ROS2, OpenCV, PCL, Python, C++[^1]

The key distinction is that the GNSS module is a separate Yahboom component based on ATGM336H-5N that supports multiple satellite systems, while the IMU is a standalone 10-axis sensor that can optionally connect to the GNSS module via its D1 port to form a complete inertial navigation unit.[^1]

<div align="center">⁂</div>

[^1]: tech_spec_2.0.pdf

