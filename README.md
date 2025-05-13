# Myra Rover - 4WD Robot Project

A versatile 4-wheel drive rover with multiple control modes and intelligent features. This project combines hardware and software components to create a robust, multi-purpose robotic platform capable of autonomous navigation, remote control, and intelligent decision-making.

![Myra Rover](/Images/1.jpg)

## Project Overview

The Myra Rover is designed with flexibility and extensibility in mind, featuring:

- Multiple control interfaces for various use cases
- Robust power management system
- Intelligent navigation capabilities
- Modular architecture for easy maintenance and upgrades

## Repository Links

- [Logic Controller](https://github.com/ShivanshGhelani/Myra-Rover-logic-controller.git) - ESP32-based logic control system
- [Motor Controller](https://github.com/ShivanshGhelani/Myra-Rover-motor-controller.git) - Motor control implementation
- [Ground Controller](https://github.com/ShivanshGhelani/Myra-Rover-motor-controller.git) - Ground station interface and remote control

## Control Modes

The Myra Rover supports multiple control modes for versatile operation:

1. **WiFi-Controlled**

   - Direct wireless control over WiFi network
2. **Voice-Controlled**

   - Voice command support through Ground Station/Controller
3. **Hand Gesture Based**

   - Gesture recognition via Ground Controller
4. **Semi-Autonomous Features**

   - Obstacle Avoidance (Partially implemented)
   - Lane Following (In Progress, using Computer Vision)

## Hardware Specifications

### Motor Control System

- **Motor Drivers:**
  - L298N (Analog Speed Controller)
  - TB6612FNG (PWM Speed Controller)

### Microcontrollers

- **ESP32 #1:**

  - Dedicated to motor control logic
  - Refer to motor control repository for implementation details
- **ESP32 #2:**

  - Handles main logic control
  - Processes commands from Ground Controller
  - Refer to logic controller repository for details

### Input Devices

- GamePAD for input control and mode switching
  - See ground control repository for implementation

## Power Requirements

### Recommended Setup

- **Motors:** 4S Battery configuration
- **Logic:** 2S Battery configuration
- **Total:** 6S configuration
- **Specifications:** 12V, 5A for optimal performance and extended operation

### Minimum Setup

- **Total:** 4S configuration
- **Specifications:** 9V, 3A
- **Note:** May experience jerky movement

### Power Management

- **Recommended Components:**

  - DC-DC Buck and Boost converters
  - 1000µF, 25V capacitor for power stabilization
  - Alternative capacitor ratings can be used based on specific buck/boost converter and battery configurations
- **Stability Measures:**

  - Use buck/boost converters for both logic and motor power
  - Capacitor implementation helps prevent power cutoffs and reboot issues

## Project Documentation and Media

### Project Images

![Hardware Setup](/Images/2.jpg)

The `/Images` folder contains detailed photographs and diagrams of:

- Complete rover assembly
- Hardware component layout
- Circuit diagrams
- Control system architecture

### Video Demonstrations

The following videos showcase the rover's basic functionality testing:

1. **Video 1** - WiFi Control Mode Testing (/Videos/1.mp4)
2. **Video 2** - Voice Control Mode Testing (/Videos/2.mp4)
3. **Video 3** - Hand Gesture Control Testing (/Videos/3.mp4)
4. **Video 4** - Basic Movement and Speed Testing (/Videos/4.mp4)

Note: Autonomous features (obstacle avoidance and lane following) are still under development and will be demonstrated in future updates.

### Technical Specifications

#### Chassis Specifications

- **Type:** 4WD Suspension Smart Car Chassis Kit
- **Dimensions:** 25 × 25 × 8 cm
- **Weight:** 1.3 kg
- **Body Material:** Acrylic

#### Motor Specifications

- **Type:** BO Motor (Dual Shaft)
- **Rated Speed:** 300 RPM
- **Operating Voltage:** 12V
- **No-Load Current:** 120mA
- **Stall Current:** 1.8A
- **Shaft Diameter:** 6mm
- **Quantity:** 4 motors (one per wheel)
- **Configuration:** 4-wheel drive with suspension

#### Wheel Specifications

- **Type:** Mecanum Wheels (Set of 4)
- **Diameter:** 80mm
- **Color:** Black
- **Material:** High-quality aluminum alloy hub with rubber rollers
- **Compatibility:** 6-7mm motor shaft

#### Coupling Specifications

- **Type:** ABS Hex Coupling
- **Size:** 6-7mm
- **Mounting:** M2.5 x 30mm screws
- **Application:** Connects mecanum wheels to motor shafts

#### Performance Metrics

- Maximum Speed: 250RPM
- Operating Time:
  - With 6S setup: 2hrs
  - With 4S setup: 1hrs
- Turning Radius: 20 degrees

### System Architecture

```
Myra Rover System Layout
├── Ground Controller
│   ├── User Interface
│   ├── Voice Recognition
│   └── Gesture Recognition
├── Logic Controller (ESP32 #2)
│   ├── Command Processing
│   ├── Sensor Integration
│   └── Decision Making
└── Motor Controller (ESP32 #1)
    ├── Motor Drivers
    ├── Speed Control
    └── Movement Coordination
```

## Development Status and Roadmap

### Current Status

- ✅ Basic motor control implementation
- ✅ Multiple control modes
- ✅ WiFi control system
- ✅ Voice control integration
- ⚠️ Partial obstacle avoidance feature
- 🚧 Lane following via Computer Vision (In Progress)

### Future Enhancements

1. **Autonomous Navigation**

   - Enhanced obstacle avoidance
   - Path planning algorithms
   - Dynamic route optimization
2. **Sensor Integration**

   - LiDAR implementation
   - Advanced proximity sensors
   - Environmental monitoring
3. **User Interface**

   - Mobile application development
   - Web-based control interface
   - Real-time telemetry display

### Known Issues

1. Power fluctuations under heavy load (Addressed with capacitor implementation)
2. Occasional WiFi connectivity drops in certain environments
3. Latency in video feed during high-speed operation

## Hardware Components and Purchase Links

### Core Components

1. **Chassis Kit**

   - [4WD Suspension Smart Car Chassis Kit](https://robu.in/product/4wd-suspension-smart-car-chassis-with-125-rpm-bo-motors-kit/)
   - Base platform with suspension system
   - Dimensions: 25 × 25 × 8 cm
2. **Motors**

   - [300 RPM Dual Shaft BO Motor (4x)](https://robu.in/product/300-rpm-dual-shaft-bo-motor-straight/)
   - 12V DC, 120mA no-load current
   - 6mm shaft diameter
3. **Wheels**

   - [80mm Mecanum Wheels (Set of 4)](https://robu.in/product/80mm-a-mecanum-wheel-compatible-with-6-7mm-coupling-pack-of-4-black/)
   - Aluminum alloy hub with rubber rollers
   - Supports omnidirectional movement
4. **Couplings**

   - [6-7mm ABS Hex Coupling (4x)](https://robu.in/product/6-7mm-abs-hex-coupling-for-mecanum-wheel-with-m2-5-x-30mm-screw/)
   - Includes M2.5 x 30mm mounting screws

### Electronics

1. **Motor Drivers** (Choose one):

   - [L298N Motor Driver](https://robu.in/product/l298n-2a-based-motor-driver-module/)
   - [TB6612FNG Dual Motor Driver](https://robu.in/product/sparkfun-motor-driver-dual-tb6612fng/)
2. **Microcontrollers**:

   - [ESP32 Development Board (2x)](https://robu.in/product/esp32-dev-kit-v1-30-pin/)
   - WiFi & Bluetooth enabled
3. **Power Management**:

   - [DC-DC Buck Converter Module](https://robu.in/product/xl4015-5a-dc-dc-step-down-adjustable-power-supply-module/)
   - [1000µF 25V Capacitor](https://robu.in/product/1000uf-25v-electrolytic-capacitor/)
4. **Batteries**:

   - Recommended: 6S Configuration (22.2V)
   - Minimum: 4S Configuration (14.8V)
   - [Li-Po Battery Options](https://robu.in/product-category/robotics-battery/)

### Sensors and Additional Components

1. **Input Device**:

   - [USB Gamepad Controller](https://robu.in/product/usb-2-0-gamepad-controller-for-pc/)
2. **Connectivity**:

   - [USB to TTL Converter](https://robu.in/product/ft232rl-usb-to-ttl-serial-converter-adapter-module/)
   - [Jumper Wires](https://robu.in/product/40-pieces-male-to-female-dupont-wire-jumper-cables-20cm/)

### Tools Required

1. [Soldering Iron Kit](https://robu.in/product/60w-soldering-iron-kit/)
2. [Wire Stripper](https://robu.in/product/automatic-wire-stripper-and-cutter/)
3. [Multimeter](https://robu.in/product/digital-multimeter-dt830l/)
4. [Basic Screwdriver Set](https://robu.in/product/jackly-31-in-1-screwdriver-set/)

Note: Links provided are for reference. You can purchase components from any reliable supplier in your region.

## Setup and Installation

### Prerequisites

1. Required Hardware:

   - ESP32 microcontrollers (2x)
   - L298N or TB6612FNG motor drivers
   - DC motors (4x)
   - Batteries (4S/6S configuration)
   - Buck/Boost converters
   - Capacitors (1000µF, 25V)
2. Development Environment:

   - Arduino IDE or PlatformIO
   - Required libraries (see each controller repository)
   - Python 3.x for Ground Station

### Assembly Instructions

1. Power System Setup

   - Battery configuration
   - Voltage regulation
   - Power distribution
2. Motor System

   - Motor mounting
   - Driver connection
   - ESP32 #1 setup
3. Control System

   - ESP32 #2 configuration
   - Sensor integration
   - Ground station setup

## Contributing

We welcome contributions to the Myra Rover project! Here's how you can help:

### Ways to Contribute

1. **Code Contributions**

   - Bug fixes
   - Feature implementations
   - Performance improvements
   - Documentation updates
2. **Testing and Feedback**

   - Hardware configurations
   - Use case scenarios
   - Performance testing
   - Bug reports

### Contribution Process

1. Fork the relevant repository
2. Create a feature branch
3. Commit your changes
4. Submit a pull request
5. Wait for review and merge

## Support and Contact

For questions, issues, or collaboration:

- Open an issue in the respective repository
- [Add contact information]
- [Add community/forum links]

## License

MIT License

Copyright (c) 2025 Myra Rover Project

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

---

<div align="center">
Made with ❤️ by Shivansh Ghelani
</div>
