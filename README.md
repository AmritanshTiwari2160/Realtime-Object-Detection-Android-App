# Real-time Object Detection using Kotlin

**Overview** <br/>
Welcome to the Real-time Object Detection project! This project leverages Kotlin and TensorFlow Lite to perform real-time object detection on Android devices. The app captures live camera feed and processes it using a pre-trained SSD MobileNet V1 model to detect and classify objects in real-time.

**Features:**
1. Real-time Object Detection: Detects objects in the camera feed in real-time with high accuracy.
2. High Performance: Optimized for performance using TensorFlow Lite.
3. Customizable: Easily switch models or modify detection parameters.
4. User-Friendly: Simple and intuitive interface.

**Code Explanation:** <br/>

*MainActivity.kt* <br/>
The `MainActivity` handles the camera feed and processes the images for object detection.

### Activity Initialization:
- Initialize the camera, machine learning model, and other components needed for real-time object detection.

### Request Camera Permissions:
- Ensure the application has permission to use the camera. If not, request the necessary permissions from the user.

### Load Labels and Prepare Image Processor:
- Load the class labels for object detection from a file.
- Set up an image processor to preprocess camera frames (resize them to the required input size for the model).

### Set Up Background Thread for Camera Operations:
- Start a background thread to handle camera operations without blocking the main UI thread.

### Initialize Camera Preview:
- Set up a `TextureView` to display the camera preview.
- Attach a listener to handle updates to the camera preview.

### Open Camera and Start Capture Session:
- Open the camera using the `CameraManager`.
- Create a capture request and set up a session to continuously capture frames from the camera.

### Process Each Frame for Object Detection:
- On each update of the camera preview:
  - Capture the current frame as a bitmap.
  - Preprocess the bitmap using the image processor.
  - Feed the preprocessed image into the TensorFlow Lite model for inference.
  - Extract the detection results (object locations, classes, and confidence scores).

### Draw Detection Results:
- For each detected object:
  - Draw a bounding box around the object.
  - Label the bounding box with the object's class name and confidence score.
- Update the `ImageView` to display the processed frame with detection results.

### Handle Camera Permission Results:
- Re-check and re-request camera permissions if they were not granted initially.

### Clean Up:
- Properly close the model and release resources when the activity is destroyed.

**Dependencies:** <br/>
1. TensorFlow Lite
2. Android Camera2 API
   
***Contributing***🤝 <br/>
Contributions are welcome! If you find a bug or want to add a feature, feel free to open an issue or submit a pull request.
