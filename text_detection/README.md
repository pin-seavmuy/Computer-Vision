# Text Detection with EasyOCR and OpenCV

This project is a simple text detection script using Python, EasyOCR, OpenCV, and Matplotlib. It reads an image, detects text within it, and draws bounding boxes along with the detected text directly on the image for visualization.

## Prerequisites

Make sure you have the required dependencies installed. You can install them using pip:

```bash
pip install -r requirements.txt
```

The dependencies include:
- `easyocr`
- `matplotlib`
- `opencv-python-headless` (or `opencv-python`)

## Project Structure

- `main.py`: The main script that loads an image, initializes the EasyOCR reader, processes the image to find text, draws bounding boxes around the detected text (for text with a confidence score > 0.25), and displays the final result using Matplotlib.
- `requirements.txt`: The file containing all the necessary Python packages to run the project.

## Usage

Simply run the main script. By default, the script reads a test image from a hardcoded path (`D:/Computuer Vision/test_image/test1.jpg`). You can change the `image_path` variable inside `main.py` to point to any image you want to test.

```bash
python main.py
```
