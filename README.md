# Real-Life-Violence-Situations

## Data Collection

The data used was data provided by Kaggle. The data is largely divided into Violence and NonViolence for 1000 images each.

[Real Life Violence Situations Data](https://www.kaggle.com/mohamedmustafa/real-life-violence-situations-dataset)


# Video Processing Script

This script is designed to process multiple video files, detect violent activities, and output the processed videos with annotations indicating the presence of violence.

## Prerequisites

Before running the script, ensure you have the following dependencies installed:

- Python (version 3.x)
- OpenCV (cv2)
- Keras
- NumPy
- Matplotlib

You can install the required Python packages using pip:
pip install opencv-python keras numpy matplotlib

## Usage

1. Clone this repository to your local machine.

2. Navigate to the directory containing the script.

3. Place your video files in the specified directory. Alternatively, you can specify the paths to your video files in the script.

4. Update the paths to the trained model and label binarizer in the script if necessary.

5. Run the script using the following command:
python video_processing_script.py

. The script will process each video file, detect violent activities, annotate the videos, and save the processed videos with the annotations in the specified output directory.

## Configuration

You can configure the script by modifying the arguments dictionary (`args`) in the script file:

- `model`: Path to the trained model file.
- `label-bin`: Path to the label binarizer file.
- `input`: Path to the input video files or specify `"camera"` for live camera input.
- `output`: Path to the output directory where processed videos will be saved.
- `size`: Size of the prediction queue.
- 
## Model
I have used `InceptionV3` which is a pretrained Imagenet CNN model provided by `Keras`.

Update - `MobileNetV2` is used to with improved accuracy and predictions. This model was created on Kaggle. 
![plot](https://github.com/Jesi1511/Real-Life-Violence-Situations/assets/144013413/7e942ab1-c4bb-4dff-a437-dc7292407e3f)
## Additional Notes

- Ensure that your input video files are in the correct format and have the appropriate file extensions (e.g., `.mp4`).
- The script assumes that the input videos contain violent activities. If your videos contain non-violent activities, you may need to adjust the detection threshold or modify the script accordingly.
- For live camera input, make sure your camera is connected and configured correctly.

## Reference
https://www.pyimagesearch.com/2019/07/15/video-classification-with-keras-and-deep-learning/
https://www.pyimagesearch.com/2019/06/03/fine-tuning-with-keras-and-deep-learning/
