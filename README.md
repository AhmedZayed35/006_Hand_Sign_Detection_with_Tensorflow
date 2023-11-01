# Hand Signs Detection Model

## Introduction

This readme provides an overview of the code and steps for training an object detection model using TensorFlow and deploying it for real-time detection from a webcam.

## Detected Objects

The object detection model is designed to recognize the following hand signs:

1. **Thumbs Up**: Represents a positive or affirmative gesture.
2. **Thumbs Down**: Signifies a negative or disapproving gesture.
3. **Thank You**: A hand sign used to express gratitude and appreciation.
4. **Live Long**: Symbolizes a wish for a long and healthy life.

## Prerequisites

Before running the code, ensure you have the following prerequisites installed:

- Python 3.10 and required dependencies.
- Protobuf Compiler (Use the provided code to install it).
- TensorFlow
- TensorFlow Object Detection API (TFOD) installed (Use the provided code).
- LabelImg for labeling images (Use the provided code).
- Webcam for real-time detection.

You can install the required packages using the requirements.txt file provided in this repository. To install the dependencies, run the following command:

```pip install -r requirements.txt```

## Code Structure

The code is divided into two notebooks: "Image Collection Notebook" and "Training and Detection Notebook". Here's an overview of what each notebook does:

### Image Collection Notebook

1. **Import Dependencies**: Installs required Python packages and imports necessary libraries.

2. **Define Images to Collect**: Specify the labels and the number of images to collect for each label.

3. **Setup Folders**: Create the folder structure for storing collected images.

4. **Capture Images**: Capture images from your webcam and save them in the specified folders.

5. **Image Labeling**: Install and use LabelImg to label the collected images.

6. **Move Images into Training and Testing Partition**: Prepare the data for model training.

### Training and Detection Notebook

1. **Setup Paths**: Define paths for various components of the project.

2. **Download TF Models Pretrained Models**: Download a pre-trained model from the TensorFlow Model Zoo.

3. **Create Label Map**: Define the labels and create a label map.

4. **Create TF Records**: Convert images and labels into TF records.

5. **Train the Model**: Train the object detection model using the collected data.

6. **Evaluate the Model**: Evaluate the trained model's performance.

7. **Load Trained Model from Checkpoint**: Load the trained model for inference.

8. **Detect from an Image**: Perform object detection on a single image.

9. **Real-Time Detections from Webcam**: Perform real-time object detection from a webcam.

10. **Freezing the Graph**: Freeze the trained model for deployment.

11. **Conversion to TFJS**: Convert the model to TensorFlow.js format for web deployment.

12. **Conversion to TFLite**: Convert the model to TensorFlow Lite format for mobile deployment.

13. **Zip and Export Models**: Archive the models for deployment.

## Running the Code

1. Open and run the "Image Collection Notebook" to collect and label images.

2. Open and run the "Training and Detection Notebook" to train the object detection model and perform real-time detection.

3. Ensure you have labeled images in the correct folder structure and the necessary configuration files.

4. You can further customize the model by adjusting hyperparameters, labels, and paths as needed.

## Real-Time Detection

The code provided allows real-time object detection from your webcam. To stop the webcam detection, press 'q' on the keyboard.

## Deployment

The code provides steps to convert the trained model for deployment in TensorFlow.js and TensorFlow Lite formats. Deploy the model as per your requirements.

## Acknowledgments

This code is based on the TensorFlow Object Detection API and various open-source contributions. Please refer to the respective repositories and documentation for additional details.
