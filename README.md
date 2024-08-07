# Street_light_proj

Centralized Monitoring System for Street Light Fault Detection and Location Tracking

Prototype - https://www.youtube.com/watch?v=8h7lmzbYSU0

Jetson Nano - https://developer.nvidia.com/embedded/learn/get-started-jetson-nano-devkit

Roboflow - It is a Computer Vision developer framework for better data collection to preprocessing, and model training techniques. Roboflow has public datasets readily available to users and has access for users to upload their own custom data also. Roboflow accepts various annotation formats. In data pre-processing, there are steps involved such as image orientations, resizing, contrasting, and data augmentations.

Steps To Use Roboflow in Object Detection: 1.Dataset_Loading 2.Labeling 3.Organise 4.Process 5.Train 6.Deploy 7.Display

For your *Centralized Monitoring System for Street Light Fault Detection and Location Tracking* project using Jetson Nano, Roboflow, and a drone, here’s a possible approach:

### Project Overview:
The goal of this project is to develop a system that can monitor street lights, detect faults, and track their location in real-time. By leveraging computer vision and AI on the Jetson Nano, along with drone technology, you can automate the detection and reporting of street light issues.

### Key Components:
1. **Jetson Nano**:
   - **Purpose**: Acts as the main processing unit for real-time image processing and AI inference.
   - **Tasks**:
     - Deploy AI models for detecting street light faults (e.g., lights off when they should be on, damaged lights).
     - Process video streams from the drone’s camera.
   
2. **Roboflow**:
   - **Purpose**: Used for dataset management, model training, and deployment.
   - **Tasks**:
     - Create or gather a dataset of street lights in different conditions (normal operation, faulty, etc.).
     - Train a computer vision model to recognize and classify these conditions.
     - Deploy the trained model to the Jetson Nano.

3. **Drone**:
   - **Purpose**: Provides a mobile platform for capturing images and videos of street lights.
   - **Tasks**:
     - Patrol pre-defined routes or respond to alerts from the system.
     - Send video feeds to the Jetson Nano for processing.
     - Utilize GPS for location tracking of detected faults.

### Implementation Steps:

1. **Dataset Creation**:
   - Collect images of street lights in various conditions.
   - Annotate the dataset with relevant labels (e.g., "light on," "light off," "damaged").
   - Use Roboflow to manage the dataset and augment it as needed.

2. **Model Training**:
   - Train a model using Roboflow’s tools, focusing on accuracy in detecting street light faults.
   - Export the model in a format compatible with the Jetson Nano (e.g., TensorRT optimized).

3. **Deployment on Jetson Nano**:
   - Set up the Jetson Nano environment with the necessary libraries (TensorFlow, OpenCV, etc.).
   - Deploy the trained model and set up a pipeline for processing video streams from the drone.

4. **Drone Integration**:
   - Equip the drone with a camera capable of streaming live video.
   - Implement a control system for the drone to follow specific routes or move towards detected issues.
   - Integrate GPS for location tracking and send coordinates of detected faults to a central monitoring station.

5. **Real-time Monitoring and Alerts**:
   - Set up a real-time monitoring dashboard that displays the status of street lights and alerts operators to detected faults.
   - Include a map interface that shows the location of any detected issues using the drone’s GPS data.

6. **Testing and Optimization**:
   - Test the system in a controlled environment, gradually moving to real-world scenarios.
   - Optimize the AI model and drone flight paths for better accuracy and efficiency.

7. **Reporting and Analytics**:
   - Implement a reporting system that logs detected faults, their locations, and the time of detection.
   - Use this data for maintenance scheduling and performance analytics.

### Challenges and Considerations:
- **Environmental Conditions**: Ensure the system is robust against different lighting conditions and weather scenarios.
- **Battery Life and Flight Time**: Optimize drone operations to maximize battery life and flight time, possibly incorporating multiple drones for larger areas.
- **Real-time Processing**: Ensure the Jetson Nano can handle real-time processing with minimal latency.

### Future Enhancements:
- Integrating additional sensors on the drone for more comprehensive monitoring (e.g., thermal cameras).
- Implementing machine learning models to predict when street lights might fail based on historical data.

This project combines cutting-edge technologies to automate the maintenance of street lights, potentially leading to more efficient and timely repairs, reducing energy wastage, and improving public safety.


