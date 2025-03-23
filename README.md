Objective
The goal of this project is to compare the performance of four different versions of the YOLOv11 object detection model — YOLOv11-S, YOLOv11-M, YOLOv11-L, and YOLOv11-X — in terms of inference time, detection accuracy, and object count. The objective is to identify the most suitable model based on speed and detection performance.

Dataset Overview
Source Image: buses.jpeg (sample image containing multiple objects).
Models Tested:
YOLOv11-S – Small model, optimized for speed and low memory usage.
YOLOv11-M – Medium-sized model, balanced between speed and accuracy.
YOLOv11-L – Large model, more accurate but slower inference.
YOLOv11-X – Extra-large model, highest accuracy but slowest inference.
Project Workflow
1. Model Loading and Prediction

✅ Installed the Ultralytics YOLO package for object detection.
✅ Loaded the pre-trained YOLOv11 models from custom .pt files.
✅ Performed inference on the sample image using each model with a confidence threshold of 0.5.
✅ Saved the detection results for visualization.

2. Post-Prediction Processing

✅ Loaded the predicted output images for all four models.
✅ Converted BGR images to RGB for proper visualization.
✅ Plotted the results using a 2x2 grid for easy comparison.

3. Performance Metrics Comparison

✅ Collected the following performance metrics for each model:

Inference Time: Time taken for the model to perform inference on the image (in milliseconds).
Objects Detected: Total number of objects detected by each model.
Confidence Threshold: Fixed at 0.5 across all models for consistency.
✅ Created a summary table using Pandas to compare model performance.

Results and Comparison
Model	Inference Time (ms)	Objects Detected	Confidence Threshold
YOLO11-S	15.2	9	0.5
YOLO11-M	22.4	12	0.5
YOLO11-L	45.8	14	0.5
YOLO11-X	78.6	16	0.5
Insights
📌 YOLO11-S:

Fastest model with lowest inference time (15.2 ms).
Suitable for real-time processing but missed some objects.
📌 YOLO11-M:

Balanced speed and accuracy (22.4 ms).
Detected more objects than YOLO11-S with minimal increase in inference time.
📌 YOLO11-L:

Higher accuracy (14 objects) but with increased inference time (45.8 ms).
Better for offline or batch processing.
📌 YOLO11-X:

Detected the most objects (16) but at the cost of very high inference time (78.6 ms).
Suitable for high-precision tasks where speed is less critical.
Performance-Accuracy Tradeoff
Model	Strength	Weakness
YOLO11-S	Fastest	Lower accuracy
YOLO11-M	Balanced	Slightly higher inference time
YOLO11-L	Higher accuracy	Increased inference time
YOLO11-X	Highest accuracy	Slowest inference time
Conclusion
✅ YOLO11-S → Best for real-time applications with low processing power.
✅ YOLO11-M → Best for a balance between accuracy and speed.
✅ YOLO11-L → Best for applications requiring higher detection accuracy.
✅ YOLO11-X → Best for high-precision tasks where speed is not a concern.
Next Steps
🔎 Test on larger datasets with varying object sizes and densities.
🔎 Fine-tune confidence thresholds and non-maximum suppression (NMS) settings.
🔎 Explore model compression and quantization to reduce inference time.
🔎 Test models on edge devices and low-power hardware.

Technologies and Tools
✅ Python
✅ OpenCV
✅ Matplotlib
✅ Ultralytics YOLO
✅ Pandas
