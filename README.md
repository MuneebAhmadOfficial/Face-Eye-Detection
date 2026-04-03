# Face-Eye-Detection
A real-time facial analysis tool using Python and OpenCV's Haar Cascade classifiers to detect human faces and eyes within uploaded images.

## 🚀 Added Features
* **Multi-Object Detection**: Simultaneously detects both the primary face and individual eyes within the detected facial region.
* **Haar Cascade Integration**: Leverages OpenCV's built-in `haarcascade_frontalface_default.xml` and `haarcascade_eye.xml` for robust feature matching.
* **Region of Interest (ROI) Optimization**: To increase accuracy and efficiency, the eye detection is restricted to the detected face region rather than the entire image.
* **Visual Annotation**: Automatically draws bounding boxes (rectangles) around detected features for clear visual confirmation.
* **Interactive Image Processing**: Built with a Google Colab interface to allow for quick testing on various portrait and group photos.

## 🗺️ Navigation Flow
The logic is divided into a structured detection pipeline:

1.  **Resource Loading**: The script imports `cv2` and `matplotlib`, and loads the XML classifier files.
2.  **User Input**: Execute the upload cell to provide a `.jpg` or `.png` containing at least one human face.
3.  **Preprocessing**: The image is converted to grayscale to simplify the detection math and improve processing speed.
4.  **Detection Phase**:
    * **Face Search**: `detectMultiScale` identifies face boundaries.
    * **Eye Search**: For every face found, the script creates a localized ROI to scan for eyes.
5.  **Annotation & Display**: Bounding boxes are rendered onto the color image, and the final result is plotted using Matplotlib.

## 🛠️ Requirements
- Python 3.x
- OpenCV (`opencv-python`)
- Matplotlib
- Haar Cascade XML files (included in OpenCV or available in the repo)

## 📖 How to Use
1. Open `LAB_06.ipynb` in Google Colab.
2. Run all cells.
3. Upload an image when prompted.
4. The output will display the image with faces outlined in one color and eyes in another.
