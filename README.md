# AI Traffic Management System

A web-based traffic detection and management simulator for monitoring and controlling traffic across two lanes with intelligent signal control.

![AI Traffic Management System](https://via.placeholder.com/800x400?text=AI+Traffic+Management+System)

## Overview

This AI Traffic Management System provides a realistic simulation of intelligent traffic control using computer vision for real-time vehicle detection and classification. The system monitors two lanes simultaneously, detecting vehicles, emergency vehicles, non-moving vehicles, and potential accidents.

## Features

- **Dual Lane Monitoring**: Real-time traffic analysis across two separate lanes
- **AI-Powered Detection**: Simulated YOLOv8 object detection for identifying various vehicle types
- **Emergency Vehicle Priority**: Automatic signal switching when emergency vehicles are detected
- **Accident Detection**: Identifies potential accidents and triggers emergency responses
- **Non-Moving Vehicle Detection**: Identifies traffic violations when vehicles don't move on green signals
- **Automated Traffic Signal Control**: Smart switching between lanes based on traffic conditions
- **Emergency Notification System**: Simulated integration with Twilio for emergency alerts
- **Comprehensive Logging**: Detailed system logs with timestamps for all events
- **Customizable Settings**: Adjustable parameters for emergency contacts and violation thresholds

## Technologies Used

- **Frontend**: HTML, CSS, JavaScript
- **AI Detection**: Simulated YOLOv8 model (could be replaced with real ONNX or TensorFlow models)
- **Video Processing**: HTML5 Canvas for detection visualization
- **Notifications**: Simulated Twilio integration for SMS and calls
- **Data Storage**: Browser localStorage (simulated MongoDB)

## How to Use

1. **Setup**:
   - Open the HTML file in any modern web browser
   - No installation required - pure client-side application

2. **Upload Traffic Videos**:
   - Click on the upload areas in each lane section
   - Select traffic video files for analysis
   - The system will automatically begin processing and detection

3. **Monitor Traffic**:
   - Watch real-time detection results in each lane
   - View system logs for events and alerts
   - Traffic signals automatically adjust based on conditions

4. **Manual Control**:
   - Click on traffic signals to manually control red/green states
   - Note that emergency vehicles will override manual settings

5. **Configure Settings**:
   - Set emergency contact numbers for alerts
   - Adjust non-moving vehicle threshold timing

## System Components

### Traffic Detector
- Simulates YOLOv8 object detection
- Classifies various vehicle types including emergency vehicles
- Detects non-moving vehicles and potential accidents

### Traffic Signal Controller
- Manages signal states for both lanes
- Implements priority rules for emergency vehicles
- Automatic switching based on traffic conditions

### Emergency Notification System
- Simulated Twilio integration for emergency calls
- SMS notifications for violations and accidents

### Data Storage
- Records violations and accidents
- Stores event data using browser localStorage

## Implementation Details

The system uses a class-based architecture with three main components:

1. **TrafficDetector**: Handles all detection logic, including object detection, vehicle tracking, and event analysis
2. **TwilioService**: Manages emergency notifications and alerts
3. **StorageService**: Handles data persistence for violations and accidents

## Development Notes

- This is a simulation with randomized detection events
- In a production system, replace the simulated detection with actual YOLOv8 inference
- Twilio integration would require backend services with proper API credentials
- Data storage would typically use a real database like MongoDB

## Future Enhancements

- Integration with real traffic cameras
- Machine learning for predictive traffic flow management
- Mobile application for remote monitoring
- Multi-intersection coordination
- Historical data analysis and reporting dashboard

## License

This project is licensed under the MIT License - see the LICENSE file for details.