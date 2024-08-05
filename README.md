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
The MainActivity handles the camera feed and processes the images for object detection.<br/>
onCreate: Initializes the camera, model, and other components.<br/>
open_camera: Opens the camera and starts the capture session.<br/>
onSurfaceTextureUpdated: Called when the camera preview is updated; processes the image and performs detection.<br/>

**Dependencies:** <br/>
1. TensorFlow Lite
2. Android Camera2 API
   
***Contributing***🤝 <br/>
Contributions are welcome! If you find a bug or want to add a feature, feel free to open an issue or submit a pull request.
