# Drawing-using-hand-Gesture
This project demonstrates an interactive application that allows drawing on the screen using hand gestures. It uses Mediapipe for hand and pose detection and OpenCV for video processing and drawing also can Erase the drwaing using 2 finger as well as you can select the color as per your choise  .

## Requirements

- Python 3.x
- OpenCV
- Mediapipe
- Scipy

## Installation

1. Clone this repository:

    ```bash
    git clone https://github.com/jayaverma21/Drawing-using-hand-Gesture.git
    cd Drawing-using-hand-Gesture
    ```

2. Install the required packages:

    ```bash
    pip install opencv-python mediapipe scipy
    ```

## Usage

1. Run the script:

    ```bash
    python body_hand_drawing.py
    ```

2. The webcam feed will open in a new window. Use the following gestures to interact:

    - **Drawing Mode**: Keep your thumb and index finger apart, and use the index finger to draw on the screen.
    - **Eraser Mode**: Bring your thumb and index finger close together to switch to eraser mode. Use the index finger to erase drawings.
    - **Color Selection Mode**: Bring your thumb and index finger close together again to switch to color selection mode. Move your index finger over the color circles at the top left corner to change the drawing color.

3. Press the 'q' key to exit the application.

## Code Overview

The main script performs the following steps:

1. Initializes Mediapipe pose, hand, and drawing modules.
2. Opens a webcam feed and reads frames in a loop.
3. Processes each frame to detect pose and hand landmarks.
4. Draws pose and hand landmarks on the frame.
5. Uses hand gestures to switch between drawing, erasing, and color selection modes:
    - **Drawing Mode**: Draws lines on a canvas based on the index finger's position.
    - **Eraser Mode**: Erases lines on the canvas when the index finger is used.
    - **Color Selection Mode**: Changes the drawing color when the index finger is moved over the color options.
6. Combines the canvas with the annotated frame and displays the result.
7. Exits the loop when the 'q' key is pressed.
