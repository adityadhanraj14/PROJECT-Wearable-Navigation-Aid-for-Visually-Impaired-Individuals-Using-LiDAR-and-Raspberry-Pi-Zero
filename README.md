# Wearable Navigation Aid for Visually Impaired Individuals Using LiDAR and Raspberry Pi Zero

## Table of Contents
1. [Introduction](#introduction)
2. [Overview](#overview)
3. [Components Required with Bill of Materials](#components-required-with-bill-of-materials)
4. [Table for Pin Connections](#table-for-pin-connections)
5. [Pinout Diagram](#pinout-diagram)
6. [Working Code](#working-code)
7. [Demo Video](#demo-video)
8. [Video Description](#video-description)
9. [Result](#result)
10. [Conclusion](#conclusion)
11. [Future Improvement](#future-improvements)
12. [Setup and Installation](#setup-and-installation)
13. [Comparison with Existing Technology (OrCam MyEye 2 Pro)](#comparison-with-existing-technology-(orcam-myeye-2-pro))

## Introduction
<p align="justify">
    Visually impaired individuals face significant challenges in navigating their surroundings, often leading to
    accidents and reduced independence. Traditional mobility aids like canes provide limited information about the
    environment, primarily detecting obstacles at ground level. To address these challenges, the "Wearable Navigation
    Aid for Visually Impaired Individuals Using LiDAR and Raspberry Pi Zero" integrates advanced technology to enhance
    mobility and safety. Central to its functionality is the integration of an AI assistant named "Alex," facilitating
    intuitive interaction. This device leverages LiDAR sensors for precise obstacle detection, a Raspberry Pi Zero for
    computational power, MPU sensors for motion tracking, GPS for location services, and GSM modules for communication.
    These components work synergistically to offer real-time feedback and haptic alerts, reducing physical interaction
    needs and providing essential features such as location tracking and emergency communication capabilities.
</p>
<p align="justify">
    Traditionally, navigating unfamiliar environments has been cumbersome and inefficient for the visually impaired.
    This technology eliminates such challenges by allowing users to navigate their surroundings with real-time obstacle
    detection and haptic feedback, reducing the need for physical interaction. The wearable navigation aid integrates
    seamlessly into daily routines, offering features such as location tracking and emergency communication through GSM
    modules. By leveraging LiDAR's precise object detection capabilities and Raspberry Pi Zero's computational power,
    coupled with intuitive interaction facilitated by the AI assistant "Alex," this project sets a new standard in
    assistive technology for the visually impaired, enhancing their independence and safety across diverse environments.
</p>


## Overview
<p align="justify">
    This project introduces an advanced wearable navigation aid designed to enhance the mobility and safety of visually
    impaired individuals. Central to its functionality are LiDAR sensors, a Raspberry Pi Zero, MPU sensors, GPS, and GSM
    modules, replacing ESP32. These components work synergistically to provide real-time obstacle detection, spatial
    awareness, and intuitive interaction through an AI assistant named "Alex."
<ul>
    <li><b>LiDAR Sensors:</b> Detect obstacles and provide spatial awareness, scanning the environment and detecting
        obstacles at various heights.</li>
    <li><b>Raspberry Pi Zero:</b> Acts as the main processing unit, handling data from all sensors and modules.</li>
    <li><b>MPU Sensors:</b> Detect orientation and movement, adjusting LiDAR scanning based on hand movements.</li>
    <li><b>GPS Module:</b> Offers location tracking and route guidance, enhancing navigation capabilities.</li>
    <li><b>GSM Module:</b> Allows for sending alerts and receiving commands, providing emergency communication features.
    </li>
    <li><b>Servo Motors:</b> Rotate LiDAR sensors for a wider field of view, ensuring comprehensive obstacle detection.
    </li>
    <li><b>Battery:</b> Powers all components, optimized for longer battery life through efficient power management
        strategies.</li>
</ul>
Users benefit from increased confidence and independence in navigating their surroundings. The integration of real-time
obstacle detection, haptic feedback, and interactive AI assistance exemplifies the practical application of wearable
technology in enhancing the quality of life for visually impaired individuals. This project showcases a pioneering
approach in IoT and wearable technology, offering a reliable and effective solution to address the mobility challenges
faced by the visually impaired community.
</p>

## Components Required with Bill of Materials
<table>
  <tr>
    <th>Item</th>
    <th>Quantity</th>
    <th>Description</th>
    <th>Links to Products</th>
  </tr>
  <tr>
    <td>Raspberry Pi 4</td>
    <td>1</td>
    <td>Single-board computer</td>
    <td><a href="https://www.raspberrypi.org/products/raspberry-pi-4-model-b/">Raspberry Pi 4</a></td>
  </tr>
  <tr>
    <td>YDLidar X2</td>
    <td>1</td>
    <td>360-degree 2D LiDAR</td>
    <td><a href="https://robu.in/product/ydlidar-x2l-range-finder/?gad_source=1&gclid=CjwKCAjwtNi0BhA1EiwAWZaANGSRj5HHg5FWiyIhRXaESyklDIacMUF7kpODNAL2sFHSsQEIeEtqkRoCTMYQAvD_BwE/">YDLidar X2</a></td>
  </tr>
  <tr>
    <td>ArduCam ToF Camera</td>
    <td>1</td>
    <td>Time-of-Flight camera</td>
    <td><a href="https://robu.in/product/arducam-time-of-flight-camera-for-raspberry-pi/">ArduCam ToF Camera</a></td>
  </tr>
  <tr>
    <td>GSM SIM 800</td>
    <td>1</td>
    <td>GSM/GPRS module for communication</td>
    <td><a href="https://mifraelectronics.com/shop/wireless-modules/gsm-modules/sim800a-quad-band-gsm-gprs-module/">GSM SIM 800</a></td>
  </tr>
  <tr>
    <td>MPU Sensor</td>
    <td>1</td>
    <td>Accelerometer and gyroscope sensor</td>
    <td><a href="https://mifraelectronics.com/shop/iot-sensors/sensors-module/accelerometer-and-gyroscope-sensor-from-mifar-electronics-store/mpu-6050-3-axis-accelerometer-and-gyroscope-sensor/">MPU Sensor</a></td>
  </tr>
  <tr>
    <td>9V Battery</td>
    <td>1</td>
    <td>Battery for power supply</td>
    <td><a href="https://robu.in/product/18650-lithium-battery-shield-v8-mobile-power-expansion-board-module-5v-3a-3v-1a-micro-usb-for-arduino-esp32-esp8266-%EF%BC%882-switch%EF%BC%89/?gad_source=1&gclid=CjwKCAjwtNi0BhA1EiwAWZaANEHsx5Ie2l1eqHJgPrN4cbGqGxEM130RNvvJ3WtiU4M4xBdZFUdqehoCiM0QAvD_BwE">9V Battery</a></td>
  </tr>
  <tr>
    <td>Microphone</td>
    <td>1</td>
    <td>Microphone for audio input</td>
    <td><a href="https://robu.in/product/microphone-97mm-pack-of-3/">Microphone</a></td>
  </tr>
  <tr>
    <td>Speaker</td>
    <td>1</td>
    <td>Speaker for audio output</td>
    <td><a href="https://robu.in/product/0-5w-8ohm-trumpet-diameter-36mm/?gad_source=1&gclid=CjwKCAjwtNi0BhA1EiwAWZaANHuaOZYx9Gw4oQvfK9lCC2rXfpl0QzlOuhfSdlxTyuw2gA2WdqCKIxoC2RIQAvD_BwE">Speaker</a></td>
  </tr>
</table>

## Table for Pin Connections
<table>
  <tr>
    <th>Component</th>
    <th>Pin on Raspberry Pi</th>
    <th>Pin Description</th>
  </tr>
  <tr>
    <td>YDLidar X2</td>
    <td>USB Port</td>
    <td>Power and Data</td>
  </tr>
  <tr>
    <td>TOF Sensor</td>
    <td>CSI Port</td>
    <td>Data Line (CSI)</td>
  </tr>
  <tr>
    <td></td>
    <td>GPIO 3 (SCL)</td>
    <td>Clock Line (SCL)</td>
  </tr>
  <tr>
    <td></td>
    <td>GPIO 2 (SDA)</td>
    <td>Data Line (SDA)</td>
  </tr>
  <tr>
    <td>GSM Module</td>
    <td>GPIO 14 (TXD)</td>
    <td>Data Transmission (TX)</td>
  </tr>
  <tr>
    <td></td>
    <td>GPIO 15 (RXD)</td>
    <td>Data Reception (RX)</td>
  </tr>
  <tr>
    <td></td>
    <td>GPIO 4</td>
    <td>Power</td>
  </tr>
  <tr>
    <td></td>
    <td>GND</td>
    <td>Ground</td>
  </tr>
</table>

## Pinout Diagram
![Pinout Diagram](assets/pinout_diagram.png.png)

## Working Code
```python
# GemTest: Interactive AI Assistant for Blind Navigation

import speech_recognition as sr
import google.generativeai as genai
import PIL.Image

# Initialize speech recognizer
recognizer = sr.Recognizer()

# Open the image for object scanning
img = PIL.Image.open('upscaled_image.jpg')

# Configure GenerativeAI API
genai.configure(api_key="AIzaSyDR1GiO72WfzSy9hyUPb6dQUIiEq0F74S4")

# Initialize GenerativeAI model for chat interaction
model = genai.GenerativeModel('gemini-1.5-flash')
chat = model.start_chat(history=[])

# Send initial message to GenerativeAI chat
chat.send_message("""
    You are a helpingbot that helps to navigate blind peoples, they might ask what's coming or in front of them, 
    or describe things in front of them. You are here to help those. 
    I will be giving you a dictionary of objects and their respective distances. 
    You should be able to answer according to their query.
""")

def gemtest(a):
    # Split the input into words
    b = a.split(" ")
    
    if b[0] == "scan":
        # If command is "scan", send image and command to GenerativeAI for object description
        response = chat.send_message([
            f"You will be given a grayscale or a black and white image with a possibly dark background. "
            f"The image might be dark, blurry, and not optimal. The environment might seem like a dark room "
            f"or nighttime, but don't mention that. Your task is to simply answer what the user asked. "
            f"Here's the prompt: {a}", 
            img
        ], stream=True)
        response.resolve()
        print(response.text)
    else:
        # Otherwise, send the user's command for response
        response = chat.send_message(f"Here's the prompt from the blind person: {a}")
        print(response.text)

def recognize_speech():
    # Adjust for ambient noise and start listening
    with sr.Microphone() as source:
        print("Adjusting for ambient noise... Please wait.")
        recognizer.adjust_for_ambient_noise(source, duration=1)
        print("Listening...")

        while True:
            try:
                # Listen for audio input
                audio = recognizer.listen(source)
                text = recognizer.recognize_google(audio)
                print(f"You said: {text}")
                gemtest(text)  # Process the recognized text
            except sr.UnknownValueError:
                print("Sorry, I could not understand the audio.")
            except sr.RequestError as e:
                print(f"Could not request results from Google Speech Recognition service; {e}")

if __name__ == "__main__":
    recognize_speech()  # Start speech recognition loop


```

```python
# Image Preprocessing Pipeline

import cv2
import numpy as np

def increase_brightness(image, value=50):
    # Increase brightness by adding a constant value to each pixel
    return cv2.convertScaleAbs(image, alpha=1, beta=value)

def unsharp_mask(image, kernel_size=(5, 5), sigma=1.0, amount=1.5, threshold=0):
    # Apply Gaussian blur to the image
    blurred = cv2.GaussianBlur(image, kernel_size, sigma)
    
    # Calculate the sharpened image
    sharpened = float(amount + 1) * image - float(amount) * blurred
    
    # Ensure the pixel values are within the valid range [0, 255]
    sharpened = np.maximum(sharpened, np.zeros(sharpened.shape))
    sharpened = np.minimum(sharpened, 255 * np.ones(sharpened.shape))
    sharpened = sharpened.round().astype(np.uint8)
    
    if threshold > 0:
        # Create a mask to apply sharpening only to the parts of the image with sufficient difference
        low_contrast_mask = np.absolute(image - blurred) < threshold
        np.copyto(sharpened, image, where=low_contrast_mask)

    return sharpened

def upscale_image(image, scale_percent=200):
    # Upscale the image by the specified scale percentage
    width = int(image.shape[1] * scale_percent / 100)
    height = int(image.shape[0] * scale_percent / 100)
    dim = (width, height)
    return cv2.resize(image, dim, interpolation=cv2.INTER_CUBIC)

# Read the image (assuming it's an RGB image but in grayscale form)
image = cv2.imread('sandal.jpg')

# Check if the image was loaded correctly
if image is None:
    print("Error loading image")
else:
    # Convert the RGB image to grayscale
    gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

    # Increase the brightness of the grayscale image
    brightened_gray_image = increase_brightness(gray_image, value=50)

    # Apply Unsharp Mask to sharpen the brightened grayscale image
    sharpened_brightened_gray_image = unsharp_mask(brightened_gray_image)

    # Convert the sharpened brightened grayscale image back to RGB
    sharpened_brightened_rgb_image = cv2.cvtColor(sharpened_brightened_gray_image, cv2.COLOR_GRAY2BGR)

    # Upscale the sharpened RGB image
    upscaled_image = upscale_image(sharpened_brightened_rgb_image, scale_percent=200)

    # Save the processed image
    cv2.imwrite('upscaled_image.jpg', upscaled_image)

    print("Images saved successfully.")
```
```python
# Real-time Object Detection and Distance Measurement with TensorFlow and Arducam TOF Camera

import os
import cv2
import numpy as np
import tensorflow.compat.v1 as tf
tf.disable_v2_behavior()
import sys
import ArducamDepthCamera as ac
import threading
import socket

# Constants for image resolution
IM_WIDTH = 1280
IM_HEIGHT = 720

# Initialize the camera type
camera_type = 'tof'

sys.path.append('..')

from utils import label_map_util
from utils import visualization_utils as vis_util

# Model configuration
MODEL_NAME = 'ssdlite_mobilenet_v2_coco_2018_05_09'
CWD_PATH = os.getcwd()
PATH_TO_CKPT = os.path.join(CWD_PATH, MODEL_NAME, 'frozen_inference_graph.pb')
PATH_TO_LABELS = os.path.join(CWD_PATH, 'data', 'mscoco_label_map.pbtxt')
NUM_CLASSES = 90

label_map = label_map_util.load_labelmap(PATH_TO_LABELS)
categories = label_map_util.convert_label_map_to_categories(label_map, max_num_classes=NUM_CLASSES, use_display_name=True)
category_index = label_map_util.create_category_index(categories)

# Load the TensorFlow model
detection_graph = tf.Graph()
with detection_graph.as_default():
    od_graph_def = tf.GraphDef()
    with tf.gfile.GFile(PATH_TO_CKPT, 'rb') as fid:
        serialized_graph = fid.read()
        od_graph_def.ParseFromString(serialized_graph)
        tf.import_graph_def(od_graph_def, name='')

    sess = tf.Session(graph=detection_graph)

# Get the input and output tensors
image_tensor = detection_graph.get_tensor_by_name('image_tensor:0')
detection_boxes = detection_graph.get_tensor_by_name('detection_boxes:0')
detection_scores = detection_graph.get_tensor_by_name('detection_scores:0')
detection_classes = detection_graph.get_tensor_by_name('detection_classes:0')
num_detections = detection_graph.get_tensor_by_name('num_detections:0')

# Set up the Arducam TOF Camera
MAX_DISTANCE = 4

def process_frame(depth_buf: np.ndarray, amplitude_buf: np.ndarray) -> np.ndarray:
    """
    Process the frame to highlight depth information and filter based on amplitude.

    Args:
    - depth_buf: Depth data from TOF camera.
    - amplitude_buf: Amplitude data from TOF camera.

    Returns:
    - Processed frame with depth and amplitude information combined.
    """
    depth_buf = np.nan_to_num(depth_buf)
    amplitude_buf[amplitude_buf <= 7] = 0
    amplitude_buf[amplitude_buf > 7] = 255
    depth_buf = (1 - (depth_buf / MAX_DISTANCE)) * 255
    depth_buf = np.clip(depth_buf, 0, 255)
    result_frame = depth_buf.astype(np.uint8) & amplitude_buf.astype(np.uint8)
    return result_frame 

class UserRect():
    """
    Class to define rectangular regions based on user interaction.
    """
    def __init__(self) -> None:
        self.start_x = 0
        self.start_y = 0
        self.end_x = 0
        self.end_y = 0

selectRect = UserRect()
followRect = UserRect()

def on_mouse(event, x, y, flags, param):
    """
    Handle mouse events for selecting and following regions of interest.
    """
    global selectRect, followRect
    if event == cv2.EVENT_LBUTTONDOWN:
        pass
    elif event == cv2.EVENT_LBUTTONUP:
        selectRect.start_x = x - 4 if x - 4 > 0 else 0
        selectRect.start_y = y - 4 if y - 4 > 0 else 0
        selectRect.end_x = x + 4 if x + 4 < IM_WIDTH else IM_WIDTH
        selectRect.end_y = y + 4 if y + 4 < IM_HEIGHT else IM_HEIGHT
    else:
        followRect.start_x = x - 4 if x - 4 > 0 else 0
        followRect.start_y = y - 4 if y - 4 > 0 else 0
        followRect.end_x = x + 4 if x + 4 < IM_WIDTH else IM_WIDTH
        followRect.end_y = y + 4 if y + 4 < IM_HEIGHT else IM_HEIGHT

# Initialize Arducam TOF Camera
cam = ac.ArducamCamera()
if cam.open(ac.TOFConnect.CSI, 0) != 0:
    print("Initialization failed")
if cam.start(ac.TOFOutput.DEPTH) != 0:
    print("Failed to start camera")
cam.setControl(ac.TOFControl.RANG, MAX_DISTANCE)
cv2.namedWindow("preview", cv2.WINDOW_AUTOSIZE)
cv2.setMouseCallback("preview", on_mouse)

# Directory to save images
SAVE_DIR = 'pic'
if not os.path.exists(SAVE_DIR):
    os.makedirs(SAVE_DIR)

# Global variable to store detected objects
detected_objects = {}

# Function to save image with timestamp and store detected objects
def save_image():
    """
    Capture an image from the TOF camera, process it for object detection,
    and save it with detected objects annotated.
    """
    global detected_objects
    frame = cam.requestFrame(200)
    if frame is not None:
        amplitude_buf = frame.getAmplitudeData()
        depth_buf = frame.getDepthData()
        cam.releaseFrame(frame)
        amplitude_buf *= (255 / 1024)
        amplitude_buf = np.clip(amplitude_buf, 0, 255)
        amplitude_buf = amplitude_buf.astype(np.uint8)
        amplitude_buf_rgb = cv2.cvtColor(amplitude_buf, cv2.COLOR_GRAY2RGB)
        filename = f"{SAVE_DIR}/img.jpg"
        cv2.imwrite(filename, amplitude_buf_rgb)
        
        # Process the frame for object detection
        frame_expanded = np.expand_dims(amplitude_buf_rgb, axis=0)
        (boxes, scores, classes, num) = sess.run(
            [detection_boxes, detection_scores, detection_classes, num_detections],
            feed_dict={image_tensor: frame_expanded}
        )

        # Reset the detected objects dictionary
        detected_objects = {}
        h, w, _ = amplitude_buf_rgb.shape
        count = 1
        for i in range(len(boxes[0])):
            if scores[0][i] > 0.30:
                ymin, xmin, ymax, xmax = boxes[0][i]
                (left, right, top, bottom) = (xmin * w, xmax * w, ymin * h, ymax * h)
                left, right, top, bottom = int(left), int(right), int(top), int(bottom)

                box_center_x = (left + right) // 2
                box_center_y = (top + bottom) // 2
                distance = depth_buf[box_center_y, box_center_x]
                class_name = category_index[classes[0][i]]['name']
                label = f"{class_name}_{count}"
                detected_objects[label] = distance
                count += 1

# Socket server to handle image capture requests
def socket_server():
    """
    Start a socket server to listen for commands and trigger image capture.
    """
    server_socket = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
    server_socket.bind(('0.0.0.0', 3000))
    server_socket.listen(1)
    print("Socket server listening on port 3000...")

    while True:
        client_socket, addr = server_socket.accept()
        print(f"Connection from {addr}")

        while True:
            data = client_socket.recv(1024).decode()
            if not data:
                break
            if data.strip().lower() == "takepic":
                save_image()
                client_socket.send(str(detected_objects).encode())

        client_socket.close()

# Variables to control image capture timing
font = cv2.FONT_HERSHEY_SIMPLEX

def camera_loop():
    """
    Continuously capture frames from the TOF camera, process them for object detection,
    and display results overlaid on the preview window.
    """
    while True:
        t1 = cv2.getTickCount()  # Start time for FPS calculation

        frame = cam.requestFrame(200)
        if frame is not None:
            depth_buf = frame.getDepthData()
            amplitude_buf = frame.getAmplitudeData()
            cam.releaseFrame(frame)
            amplitude_buf *= (255 / 1024)
            amplitude_buf = np.clip(amplitude_buf, 0, 255)
            amplitude_buf = amplitude_buf.astype(np.uint8)

            # Convert grayscale amplitude image to RGB
            amplitude_buf_rgb = cv2.cvtColor(amplitude_buf, cv2.COLOR_GRAY2RGB)

            result_image = process_frame(depth_buf, amplitude_buf)
            result_image = cv2.applyColorMap(result_image, cv2.COLORMAP_JET)

            cv2.rectangle(amplitude_buf_rgb, (selectRect.start_x, selectRect.start_y), (selectRect.end_x, selectRect.end_y), (128, 128, 128), 1)
            cv2.rectangle(amplitude_buf_rgb, (followRect.start_x, followRect.start_y), (followRect.end_x, followRect.end_y), (255, 255, 255), 1)

            # Convert amplitude_buf_rgb for object detection
            frame_expanded = np.expand_dims(amplitude_buf_rgb, axis=0)

            # Run object detection
            (boxes, scores, classes, num) = sess.run(
                [detection_boxes, detection_scores, detection_classes, num_detections],
                feed_dict={image_tensor: frame_expanded}
            )

            # Visualization of the results of a detection
            vis_util.visualize_boxes_and_labels_on_image_array(
                amplitude_buf_rgb,
                np.squeeze(boxes),
                np.squeeze(classes).astype(np.int32),
                np.squeeze(scores),
                category_index,
                use_normalized_coordinates=True,
                line_thickness=4,
                min_score_thresh=0.30
            )

            # Display FPS
            fps = cv2.getTickFrequency() / (cv2.getTickCount() - t1)
            cv2.putText(amplitude_buf_rgb, f"FPS : {int(fps)}", (10, 30), font, 1, (0, 255, 0), 2, cv2.LINE_AA)

            # Display the resulting frame
            cv2.imshow('preview', amplitude_buf_rgb)

            # Handle keyboard input
            key = cv2.waitKey(1) & 0xFF
            if key == ord('q'):
                break
            elif key == ord('s'):
                save_image()
            elif key == ord('t'):
                threading.Thread(target=save_image).start()
        
        # Update the window and check for keyboard input
        cv2.waitKey(1)

# Start threads for camera loop and socket server
threading.Thread(target=camera_loop).start()
threading.Thread(target=socket_server).start()

# Clean up
cam.close()
cv2.destroyAllWindows()



```

## Demo Video
https://github.com/adityadhanraj14/PROJECT-Wearable-Navigation-Aid-for-Visually-Impaired-Individuals-Using-LiDAR-and-Raspberry-Pi-Zero/blob/main/assets/demo.mp4

## Video Description
<h4>Features</h4>
<ul>
    <li><b>Real-time Object Detection::</b> Our device uses a TOF camera to detect objects in real time. It provides
        accurate
        information about obstacles, including their exact distance, helping users navigate safely.</li>
    <li><b>Voice Command Interaction::</b> Users can interact with the device using voice commands. The built-in LLM
        model
        (Gemini) responds promptly, providing detailed information about the surroundings.</li>
    <li><b>Multilingual Support::</b> The device supports multiple languages, breaking language barriers and making it
        accessible to a wider audience.</li>
    <li><b>Communication Capabilities::</b> In addition to navigation, the device allows users to make calls and send
        messages
        via voice commands, ensuring they stay connected at all times.</li>
    <li><b>Privacy-focused:</b> The TOF camera ensures user privacy by avoiding the capture of real images, focusing
        solely on
        depth data for object detection.</li>
</ul>

<h4>Demonstration</h4>
<ul>
    <li><b>Wearing the Device:</b> Watch as we demonstrate the ease of use by wearing the headphone and interacting with
        the device.</li>
    <li><b>Giving Commands:</b> See how simple it is to give voice commands and receive accurate, real-time responses
        from
        Gemini. Whether it's identifying an obstacle or asking for navigation assistance, Gemini is here to help.
    </li>
    <li><b>Object Detection in Action:</b> Experience the device's precision as it detects objects and provides their
        exact
        distance, guiding you safely through your environment.</li>
    <li><b>Making Calls and Sending Messages:</b> Witness the convenience of making calls and sending messages using
        voice
        commands, ensuring you stay connected without any hassle.</li>
    <li><b>Multilingual Interaction:</b> The device's ability to understand and respond in multiple languages is
        showcased,
        demonstrating its accessibility and versatility.</li>
</ul>

## Result

The navigation device for the blind, powered by a Raspberry Pi 4, TOF camera, and advanced machine learning models, has
successfully demonstrated the following key outcomes:

- Real-time object detection with accurate obstacle distance measurement.
- Seamless voice command interaction using the LLM model (Gemini).
- Multilingual support for wider accessibility.
- Communication capabilities including voice-controlled calls and messaging.
- Privacy-focused operation using TOF camera for depth-based object detection.

## Conclusion

In conclusion, our navigation device represents a significant advancement in assistive technology for the blind,
combining state-of-the-art hardware and software components to provide real-time navigation assistance. The integration
of object detection, distance measurement, and interactive voice command capabilities ensures enhanced safety and
independence for users. With its privacy-focused design and multi-language support, the device stands out as a versatile
tool for navigating complex environments.

## Future Improvements

As we continue to enhance our navigation device for the blind, here are some planned improvements and features:

- **Compact Design**: Exploring smaller form factors, possibly leveraging bone-conduction earphones for integrated audio
feedback.

- **Cloud Integration**: Offloading computational tasks to the cloud to reduce device size and improve real-time
processing capabilities.

- **Facial Recognition**: Incorporating facial recognition technology to enhance personalization and security features.

- **Reduced Latency**: Optimizing system responsiveness to reduce latency in object detection and navigation assistance.

- **Enhanced User Interface**: Developing a more intuitive user interface for seamless interaction and accessibility.

- **Battery Efficiency**: Improving power management and exploring energy-efficient components for extended usage times.

These enhancements aim to further elevate the device's functionality, usability, and accessibility for users.

## Setup and Installation

### Prerequisites

- Python 3.x installed on your system.
- Access to a microphone for input.
- Google API key for speech recognition.
- GenerativeAI API key for interactive chat capabilities.

### Installation Steps

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/GemTest.git
   cd GemTest
2. **Install dependencies:** <br>
    ```bash
    pip install -r requirements.txt
    ```
3. **Obtain API keys:** <br>
Google API key: Obtain from Google Developer Console.
GenerativeAI API key: Obtain from GenerativeAI Dashboard.

4. **Configure API keys:** <br>
Replace placeholders in GemTest.py with your actual API keys:
    ```python
        genai.configure(api_key="YOUR_GENERATIVEAI_API_KEY")
    ```
    ```python
        recognizer = sr.Recognizer()
    ```
5. **Prepare image:** <br>
Ensure upscaled_image.jpg is in the same directory as GemTest.py. This image is used for object descriptions.




## Comparison with Existing Technology (OrCam MyEye 2 Pro)

##### Merits of OrCam MyEye 2 Pro
- **Seamless Text Accessibility**: OrCam MyEye 2 Pro provides extensive reading capabilities, including text from books, screens, and more, activated by voice, gestures, or touch.
- **Personal Reading Assistant**: It allows users to set their reading pace and preferences, making it versatile for various reading needs.
- **Object and Face Recognition**: The device can identify objects, recognize faces, and differentiate colors, enhancing daily independence.
- **Accessibility Features**: Supports voice commands, making it accessible for users with various abilities.

##### Demerits of OrCam MyEye 2 Pro
- **Limited Navigation Focus**: OrCam MyEye 2 Pro primarily focuses on text and object recognition rather than comprehensive navigation and obstacle detection.
- **Lack of Distance Accuracy**: It lacks precise distance measurement capabilities for obstacles, relying on a standard camera rather than a depth-sensing technology like your TOF camera.
- **Privacy Concerns**: OrCam MyEye 2 Pro uses a regular camera for image capture, potentially raising privacy concerns as it captures actual images rather than focusing solely on depth data.
- **High Cost**: The OrCam MyEye 2 Pro is priced significantly higher, making it less accessible for widespread adoption compared to your cost-effective solution.
- **Limited AI Capabilities**: It lacks advanced AI capabilities for real-time interaction and dynamic responses compared to the integrated LLM model (Gemini) in your device.
- **Complexity in Usage**: The interface and operation of OrCam MyEye 2 Pro may be less intuitive and tailored specifically for navigation tasks compared to your device's user-friendly voice-command interface.
