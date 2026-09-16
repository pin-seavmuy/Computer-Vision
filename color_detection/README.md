# Color Detection with OpenCV

This project is a simple real-time color detection script using Python, OpenCV, and Pillow. It captures video from your webcam and draws a bounding box around any object matching the specified color (currently set to yellow).

## Prerequisites

Make sure you have the required dependencies installed. You can install them using pip:

```bash
pip install -r requirements.txt
```

The dependencies include:
- `opencv-python`
- `numpy`
- `Pillow`

## Project Structure

- `main.py`: The main script that captures video from the webcam, processes each frame to detect the color, and displays the result with a bounding box.
- `util.py`: Contains utility functions, such as `get_limits(color)`, which calculates the upper and lower HSV limits for the color you want to detect.
- `requirements.txt`: Lists the Python packages required to run the project.

## How It Works

1. The script reads the webcam feed frame by frame.
2. It converts the color space of the frame from BGR (OpenCV's default) to HSV (Hue, Saturation, Value), which is much better for color segmentation.
3. The `get_limits()` function creates a lower and upper bound for the target color in the HSV color space.
4. A mask is created to filter out everything in the frame except the target color.
5. The bounding box of the detected area is calculated using Pillow.
6. A green rectangle is drawn around the detected object using OpenCV.

## Usage

To run the program, simply execute the `main.py` file from your terminal:

```bash
python main.py
```

- A window will pop up showing your webcam feed.
- Hold up a yellow object to the camera to see the bounding box track it!
- To exit the program, press the `q` key.

## Customizing the Color

By default, the script detects yellow:
```python
yellow = [0, 255, 255]   # yellow in BGR colorspace
```

If you want to detect a different color, you can change the RGB/BGR values in `main.py` before passing it to `get_limits()`.
