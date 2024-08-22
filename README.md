
# Object Detection and Tracking with YOLOv4-Tiny

This project demonstrates real-time object detection and tracking using the YOLOv4-Tiny model with OpenCV's DNN module. The project can process video input either from a live camera feed or a pre-recorded video file, resizing the frames and detecting objects in real-time.

## Features

- **Real-time Object Detection**: Detect objects in real-time using the lightweight YOLOv4-Tiny model.
- **Flexible Input Sizes**: Experiment with different input sizes (320x320, 416x416, 608x608) for balancing speed and accuracy.
- **Customizable Scaling**: Adjust the scaling factor to experiment with different model sensitivities.
- **Video Source Flexibility**: Switch between live camera input or pre-recorded video files.
- **High-Resolution Frame Resizing**: Resize frames to custom resolutions (e.g., 1920x1080) for better visualization.

## Setup

1. **Clone the Repository**: 
   ```bash
   git clone https://github.com/yourusername/object-detection-yolov4-tiny.git
   cd object-detection-yolov4-tiny
   ```

2. **Install Dependencies**:
   Ensure you have Python installed, then install the required libraries:
   ```bash
   pip install opencv-python
   ```

3. **Download YOLOv4-Tiny Model**:
   - Download the YOLOv4-Tiny weights and configuration files from the official YOLO website or use the links provided in the `dnn_model` folder.
   - Place the `yolov4-tiny.weights`, `yolov4-tiny.cfg`, and `classes.txt` files in the `dnn_model` directory.

## Running the Project

1. **Edit the Source File**:
   - If you want to change the video source, modify the `camera_index` or video file path in the code.
   - Adjust input size or scaling parameters as needed.

2. **Run the Script**:
   ```bash
   python object_detection.py
   ```

3. **Exit**: 
   Press the `Esc` key to exit the application.

## File Structure

```
object-detection-yolov4-tiny/
│
├── dnn_model/
│   ├── yolov4-tiny.weights
│   ├── yolov4-tiny.cfg
│   └── classes.txt
│
└── object_detection.py
```

## Customization

- **Input Size**: Adjust the `model.setInputParams(size=(320, 320), scale=1/255)` to your desired input size.
- **Scaling Factor**: Change the `scale` value to modify model sensitivity.
- **Resolution**: Modify `new_width` and `new_height` for different output resolutions.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [YOLO](https://pjreddie.com/darknet/yolo/) - You Only Look Once, a fast object detection model.
- [OpenCV](https://opencv.org/) - Open Source Computer Vision Library.
