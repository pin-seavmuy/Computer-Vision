# Virtual Drag and Drop

An interactive computer vision application that allows you to grab, drag, and drop virtual objects (rectangles) on your screen using simple hand gestures! 

Built with Python, OpenCV, and cvzone, this project tracks your hand landmarks in real-time through your webcam.

## Features
- **Real-Time Hand Tracking**: Uses `cvzone.HandTrackingModule` (powered by MediaPipe) to detect and track your hand.
- **Pinch-to-Grab**: Bring your index finger and thumb close together (distance < 30) while hovering over a rectangle to grab it.
- **Visual Feedback**: Rectangles feature a sleek semi-transparent UI with rounded corners. The active dragged rectangle turns green, while the stationary ones remain purple.
- **Overlap Handling**: Only the top-most rectangle is dragged when multiple objects overlap, preventing fused dragging glitches.

## Prerequisites

Ensure you have Python installed. It is highly recommended to use the latest compatible versions of the dependencies.

Install the required libraries via `pip`:
```bash
pip install opencv-python numpy
pip install cvzone==2.0.0
pip install mediapipe==1.0.1
```
*(Note: Older versions of `cvzone` (1.x) and `mediapipe` (0.10.x) may have incompatible APIs. Using cvzone v2+ and mediapipe v1+ is recommended for this project.)*

## How to Run

1. Clone or download this project folder.
2. Navigate to the project directory in your terminal:
   ```bash
   cd virtual_drag_drop
   ```
3. Run the main script:
   ```bash
   python main.py
   ```
4. A webcam window will open showing 5 purple rectangles.
5. Hold your hand up to the camera. Hover your index finger tip over a rectangle, pinch your index and thumb together, and move your hand to drag the rectangle around!

## Troubleshooting
- **No Webcam Feed**: Ensure your webcam is properly connected and not being used by another application (like Zoom or Teams). If you have multiple webcams, you may need to change the `cv2.VideoCapture(0)` parameter to `1` or `2`.
- **MediaPipe / cvzone Errors**: If you encounter `NameError` or `AttributeError` relating to `solutions` or `draw`, make sure you updated your packages to the versions specified above!

## License
MIT
