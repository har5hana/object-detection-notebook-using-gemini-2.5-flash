Object Detection with Gemini & OpenCV
This project demonstrates an end-to-end workflow for detecting objects within images, categorizing them, and refining results using Non-Maximum Suppression (NMS). It is designed to work with model-generated detection data (like that from Gemini 2.0/2.5 Flash) and visualize it using standard Python libraries.
🚀 Features
•	Dynamic Visualization: Automatically draws bounding boxes and labels on images using OpenCV.
•	Smart Categorization: Groups detected objects into logical categories (e.g., Electronics, Furniture, Decor) with unique color coding.
•	Non-Maximum Suppression (NMS): Includes a custom implementation to remove redundant, overlapping bounding boxes for cleaner output.
•	Matplotlib Integration: Seamlessly displays results within the Jupyter Notebook environment.
________________________________________
🛠️ Tech Stack
•	Python 3.x
•	OpenCV (cv2): For image processing and drawing.
•	Matplotlib: For rendering and displaying images.
•	NumPy: For handling coordinate arrays and mathematical operations.
________________________________________
📁 Project Structure
•	object_detection.ipynb: The main notebook containing the detection logic, NMS algorithm, and visualization code.
•	sample_image.jpg: The default input image used for testing the detection pipeline.
•	venv/: (Optional) Virtual environment containing project dependencies.
________________________________________
⚙️ How It Works
1.	Data Input: The script takes a list of detected objects, each containing a label and a box_2d (coordinates in $[y_{min}, x_{min}, y_{max}, x_{max}]$ or $[x_1, y_1, x_2, y_2]$ format).
2.	Coordinate Scaling: It converts normalized coordinates to pixel values based on the input image dimensions.
3.	Refinement (NMS): If multiple boxes detect the same object, the NMS function calculates the Intersection over Union (IoU):
$$\text{IoU} = \frac{\text{Area of Overlap}}{\text{Area of Union}}$$
Boxes with an IoU above a certain threshold are merged or removed.
4.	Output: A processed image is displayed with color-coded boxes and labels.

