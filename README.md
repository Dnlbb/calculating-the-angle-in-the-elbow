# Pose Analysis with MediaPipe and OpenCV
This application uses OpenCV and MediaPipe libraries to analyze human poses in real-time through the computer's webcam. It calculates and displays the angle at the elbow joint of the left arm.
## Prerequisites
Ensure you have Python installed on your system. You will also need the following packages:
* OpenCV
* MediaPipe
* NumPy
You can install them using pip:
```bash
pip install opencv-python mediapipe numpy
```
## Running the Application
To run the application, simply execute the script:
```bash
python pose_analysis.py
```
Make sure your webcam is connected and functioning, as the script will attempt to capture video input.
## Program Overview
The script performs the following steps:
* Initializes the webcam to capture video.
* Processes each frame to detect human pose using MediaPipe's Pose solution.
* Calculates the angle between the shoulder, elbow, and wrist of the left arm.
* Displays this angle on the frame.
* Highlights the pose landmarks and their connections on the video.
* Displays a message indicating whether the elbow angle is less than or greater than 90 degrees.
## Understanding the Code
### Initialization
* MediaPipe's Pose module is configured with specific parameters for real-time performance.
* OpenCV is used to capture video frames from the webcam.
### Main Loop
* Each frame is processed to detect pose landmarks.
* If landmarks are detected, calculates the angle at the elbow using the positions of the shoulder, elbow, wrist.
* Draws the landmarks and connections using MediaPipe's drawing utilities.
* Displays the angle and a message about its value on the screen.
### Clean-up
* Releases the webcam and destroys all OpenCV windows when the program is terminated.
## Customization
You can modify the landmark points to calculate angles for different parts of the body by adjusting the indices used for the shoulder, elbow, and wrist.

Feel free to explore other MediaPipe solutions and expand this application as needed!


