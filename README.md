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

#### Dimensions and Weight

- Length: [Add length]
- Width: [Add width]
- Height: [Add height]
- Weight: [Add weight]
- Ground Clearance: [Add clearance]

#### Performance Metrics

- Maximum Speed: [Add speed]
- Operating Time:
  - With 6S setup: [Add duration]
  - With 4S setup: [Add duration]
- Turning Radius: [Add radius]
- Maximum Incline: [Add angle]

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

## Acknowledgments

- [Add credits and acknowledgments]
- [Add references to any third-party resources]
- [Add inspiration sources]

---

<div align="center">
Made with ❤️ by Shivansh Ghelani
</div>
