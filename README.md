# **VisionEdge: Real-Time Object Detection on ESP32-CAM**

## **Overview**
Welcome to **VisionEdge**, an innovative and lightweight real-time object detection system powered by **ESP32-CAM** and optimized with **Edge Impulse**. By deploying a TinyML-based YOLO model, VisionEdge brings computer vision directly to low-power edge devices, enabling smart, autonomous, and efficient detection without the need for heavy hardware or cloud dependency.

---

## **Project Highlights**
- **Compact and Efficient**: Runs real-time object detection on an ESP32-CAM with limited memory.
- **Optimized AI Models**: Uses Edge Impulse to train and deploy lightweight YOLO models.
- **Live Video Streaming**: Captures and processes camera feed for object recognition.
- **Edge AI Application**: Enables vision-based applications in robotics, IoT, and smart systems.
- **Low-Cost Deployment**: Utilizes affordable hardware and open-source software.

---

## **Components Required**
### **Hardware**
1. ESP32-CAM module with OV2640 camera.
2. USB-to-Serial adapter for programming ESP32-CAM.
3. Breadboard and Jumper wires.
4. Power supply (5V USB or battery).

### **Software**
1. **Arduino IDE** (with ESP32 Board Manager installed).
2. **Edge Impulse Studio** (for model training and deployment).
3. **Edge Impulse CLI** (to interact with the ESP32-CAM).
4. Libraries: OpenCV, Edge Impulse SDK (automatically generated).

---

## **Installation and Setup**
### **1. Install Prerequisites**
- Install Arduino IDE and add the ESP32 Board Manager:
   - **Preferences > Additional Board URL**:
     ```
     https://dl.espressif.com/dl/package_esp32_index.json
     ```
   - Install ESP32 board from **Tools > Board Manager**.

- Install Edge Impulse CLI:
   ```bash
   npm install -g edge-impulse-cli
   ```

### **2. Setup Edge Impulse**
1. Sign up on [Edge Impulse Studio](https://www.edgeimpulse.com/).
2. Create a new project and select **Object Detection** as the learning block.
3. Connect ESP32-CAM to Edge Impulse CLI for live data collection:
   ```bash
   edge-impulse-daemon
   ```
4. Upload and annotate image data (e.g., ball, car, bottle).

### **3. Train and Deploy the Model**
1. Train a lightweight YOLO or MobileNet model optimized for Edge AI.
2. Export the model as an **Arduino Library** from Edge Impulse.
3. Integrate the exported library into your Arduino sketch.

### **4. Program the ESP32-CAM**
- Use the Arduino code to:
   - Capture video frames from the camera.
   - Run object detection inference locally.
   - Stream detection results over serial output or Wi-Fi.

---

## **Circuit Connections**
- **ESP32-CAM Pinouts**:
   - GND → GND
   - 5V → VCC
   - GPIO0 → GND (for programming mode)
   - TX → RX (USB-Serial)
   - RX → TX (USB-Serial)

**Power**: Use a 5V battery or USB adapter to power the ESP32-CAM.

---

## **How It Works**
1. **Capture Frame**: ESP32-CAM captures live video frames using the OV2640 camera.
2. **Run Inference**: The Edge Impulse TinyML model processes frames to detect specific objects.
3. **Results**:
   - Detected objects' names, confidence scores, and bounding box details are displayed.
   - Stream results via Wi-Fi or observe serial output.

---

## **Applications**
- **Robotics**: Vision-based navigation and obstacle detection.
- **Home Automation**: Detect objects for smart home solutions.
- **Surveillance**: Real-time monitoring with lightweight hardware.
- **IoT Devices**: Low-power edge AI applications for remote systems.
- **Autonomous Vehicles**: Object detection for motion control.

---

## **Challenges and Solutions**
| **Challenge**                  | **Solution**                            |
|--------------------------------|-----------------------------------------|
| Limited memory on ESP32-CAM    | Use model quantization (8-bit int)      |
| Low frame rates                | Optimize model size and inference code  |
| Lighting variations            | Train with diverse lighting conditions  |

---

## **Future Enhancements**
1. Integrate ultrasonic sensors for obstacle detection.
2. Add MQTT for real-time alerts to mobile apps.
3. Implement multiple object detection capabilities.
4. Deploy on other edge hardware like Raspberry Pi Pico or Jetson Nano.

---

## **Demo Video**
Watch the project in action on YouTube:  
[**VisionEdge Object Detection Demo**](https://youtu.be/your-video-link)

---

## **Contributors**
- **Your Name** Sourav Agrawal
- **Team Members** Rajdeep Mohanty

---

## **Acknowledgments**
- **Edge Impulse** for empowering AI on edge devices.
- **Espressif** for ESP32-CAM hardware and tools.
- **Open-source communities** for resources and libraries.

---

**VisionEdge**: Empowering Edge AI for Real-Time Object Detection 🚀

