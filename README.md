**Object Detection with Gemini & OpenCV**

This project demonstrates an end-to-end workflow for detecting objects in images, categorizing them, and refining results using Non-Maximum Suppression (NMS). It is designed to work with model-generated detection data (such as outputs from Gemini 2.0/2.5 Flash) and visualize the results using standard Python libraries.

**Features**
Dynamic visualization that draws bounding boxes and labels on images using OpenCV
Smart categorization of detected objects into groups such as Electronics, Furniture, and Decor, with distinct color coding
Custom implementation of Non-Maximum Suppression (NMS) to eliminate redundant and overlapping bounding boxes
Integration with Matplotlib for displaying results within a Jupyter Notebook environment

**Tech Stack**
Python 3.x
OpenCV (cv2) for image processing and annotation
Matplotlib for rendering and visualization
NumPy for numerical operations and coordinate handling

**Project Structure**
object_detection.ipynb – Main notebook containing detection logic, NMS implementation, and visualization
sample_image.jpg – Input image used for testing the detection pipeline
venv/ – Optional virtual environment for managing dependencies

**How It Works**
The system begins by taking a list of detected objects, where each object includes a label and bounding box coordinates. These coordinates may be in normalized format or pixel format.

The coordinates are then scaled to match the actual dimensions of the input image.

To improve detection quality, Non-Maximum Suppression (NMS) is applied. This process removes duplicate or overlapping bounding boxes by calculating the Intersection over Union (IoU), which measures how much two boxes overlap relative to their combined area. Boxes exceeding a defined overlap threshold are filtered out.

Finally, the processed image is displayed with clearly marked, color-coded bounding boxes and corresponding labels, providing a clean and interpretable output.
