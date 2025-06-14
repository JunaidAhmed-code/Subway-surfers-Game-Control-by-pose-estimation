Subway Surfers Pose Control
Description
Subway Surfers Pose Control is an innovative project that allows players to control the Subway Surfers game using body movements captured through a webcam. By leveraging MediaPipe's pose detection and OpenCV, the project translates physical gestures—such as joining hands, shifting shoulders left or right, and jumping or crouching—into keyboard inputs for game navigation. This addresses the limitations of traditional keyboard-based gaming by providing a hands-free, immersive, and interactive experience, ideal for those exploring computer vision or motion-based game control.
Installation/Usage
Installation

Clone the Repository:
git clone https://github.com/your-username/subway-surfers-pose-control.git
cd subway-surfers-pose-control


Install Dependencies:Ensure Python 3.7 or higher is installed, then install the required libraries:
pip install opencv-python mediapipe pyautogui matplotlib numpy


Set Up the Game:

Install Subway Surfers on your computer and confirm it responds to keyboard inputs.
Adjust the click coordinates (pyautogui.click(x=1300, y=800)) in the script to match the game window's start button position on your screen.



Usage

Run the Script:
python subway_surfers_pose.py


Control the Game:

Start Game/Jump: Join both hands (bring wrists close together) for a few frames to start the game or trigger a jump (spacebar).
Move Left/Right: Shift your shoulders left or right to move the character side-to-side.
Jump/Crouch: Move your shoulders upward (jump) or downward (crouch) relative to the calibrated midpoint.
Exit: Press Esc to stop the script and close the webcam feed.


On-Screen Feedback:

The webcam feed displays:
Pose landmarks (if detected).
Hand status ("Hands Joined" or "Hands Not Joined").
Horizontal position ("Left", "Right", or "Center").
Posture ("Jumping", "Crouching", or "Standing").
Frames per second (FPS).





Technologies Used

Python: Core programming language for the project.
OpenCV: Handles webcam video capture and image processing.
MediaPipe: Enables real-time pose detection and landmark tracking.
PyAutoGUI: Simulates keyboard and mouse inputs for game control.
Matplotlib: Supports optional visualization during debugging.
NumPy: Facilitates mathematical computations, such as Euclidean distance.

Challenges & Learning

Challenge: Ensuring reliable pose detection under varying lighting conditions and backgrounds.
Solution: Tuned MediaPipe's min_detection_confidence and min_tracking_confidence parameters to optimize accuracy and performance.


Challenge: Calibrating the vertical midpoint (MID_Y) for jump/crouch detection across diverse users and camera setups.
Solution: Dynamically computed MID_Y when hands are joined to start the game, ensuring adaptability.


Learning: Acquired practical experience in building computer vision pipelines, integrating MediaPipe's pose estimation with real-time game control, and managing asynchronous input simulation using PyAutoGUI.
