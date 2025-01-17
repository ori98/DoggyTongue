# DoggyTongue

**DoggyTongue** is an innovative Android app developed for Traditional Chinese Medicine (TCM) research. The app captures, processes, and analyzes tongue images from facial photos, utilizing advanced image segmentation techniques to assist in TCM diagnosis.

## Citation
When using this resource, please cite the original publication: 

Orijit Bhattacharya, QingQing Liu, Hwei Jen Lin and Chen-Hsiang Yu. "DoggyTongue: Automate Tongue Segmentation for TCM Diagnosis." 2024 IEEE International Conference on E-health Networking, Applications & Services (IEEE Healthcom 2024), November 2024.

## 📱 App Structure

DoggyTongue is composed of two core components:

1. **Android App**: Handles the user interface, captures face images using the camera, crops the tongue area, and sends it to the Flask server for processing.

2. **Flask Server**: Runs on a specified port, receives images from the Android app, segments the tongue using custom algorithms, and sends the processed images back.

## 🛠️ Workflow

1. **Image Capture & Cropping**: The Android app captures a photo of a person’s face, then crops the image to focus on the tongue.

2. **Communication with Flask Server**: The cropped image is sent to the server for further analysis.

3. **Image Segmentation**:
   - The Flask server hosts two Python scripts:
     - **`main.py`**: Sets up the server, handles incoming image data, and coordinates processing tasks.
     - **`tongue_mask.py`**: Contains the `process_image` class, which executes tongue segmentation on the received images.

4. **Result Feedback**: The segmented image is returned to the Android app, completing the cycle.

## 🚀 Key Features

- **Efficient Image Processing**: Quickly captures and processes tongue images with a streamlined workflow.
- **Advanced Segmentation**: Utilizes custom segmentation algorithms to accurately identify the tongue region.
- **Real-time Interaction**: Provides instant feedback to the user through the Android app.

## 📂 Repository Structure

- **`android_app/`**: Contains the Android source code for capturing, cropping, and sending images.
- **`flask_server/`**: Houses the server code:
  - `main.py`: Initializes the Flask server.
  - `tongue_mask.py`: Implements the image segmentation logic.

## ⚙️ Installation & Setup

1. **Android App**: Clone the repository and build the app using Android Studio.
2. **Flask Server**: Navigate to the `flask_server/` directory and run:
   ```bash
   python main.py
Ensure that all dependencies listed in requirements.txt are installed

## Publications
### DoggyTongue: Automate Tongue Segmentation for TCM Diagnosis
**Authors**: Orijit Bhattacharya, QingQing Liu, Hwei Jen Lin, Chen-Hsiang Yu  
**Conference**: 2024 IEEE International Conference on E-health Networking, Applications & Services (IEEE Healthcom 2024)  
**Date**: November 2024  

**Description**:  
This paper presents an automated approach to tongue segmentation for Traditional Chinese Medicine (TCM) diagnosis using deep learning techniques. The model enhances accuracy and efficiency in TCM practices by automating tongue image analysis.

**Status**: Accepted for presentation at IEEE Healthcom 2024.  

📄 [IEEE Healthcom 2024](https://www.ieee-healthcom.org/)  

---

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.  