# YOLOv5_moon_mars_crater_detection

# Moon Crater Detection Using YOLOv5

## Project Overview
This project leverages the YOLOv5 architecture for detecting and classifying moon craters. The model is trained on a custom dataset to achieve high accuracy in identifying craters, which has applications in planetary science and autonomous space exploration.

##Architecture
YOLOv5 (You Only Look Once, version 5) is a state-of-the-art object detection model designed for real-time applications. It processes images in a single pass, leveraging a CSPDarknet53 backbone for efficient feature extraction and a Path Aggregation Network (PANet) for multi-scale feature fusion. The model predicts bounding boxes, object classes, and confidence scores using three detection layers, ensuring accuracy across objects of varying sizes. YOLOv5 is optimized for speed and performance with advanced techniques like mosaic augmentation, anchor auto-learning, and batch normalization, making it lightweight and ideal for applications ranging from autonomous vehicles to edge devices.

## Key Features
- **YOLOv5 Model**: Utilizes a state-of-the-art object detection architecture known for its speed and accuracy.
- **Custom Dataset**: Includes over 1,500 annotated moon crater images, with extensive augmentation techniques applied.
- **Real-Time Inference**: The model achieves an average inference time of 0.5 seconds, making it suitable for deployment in real-world applications.
- **High Performance**: Achieved a mean Average Precision (mAP) of 0.85 and an Average Precision (AP) of 0.92 during validation.

## Project Workflow
1. **Setup**:
   - Cloned the YOLOv5 repository from [Ultralytics](https://github.com/ultralytics/yolov5).
   - Installed dependencies and configured the environment.

2. **Dataset Preparation**:
   - Annotated a dataset of 1,500+ moon crater images.
   - Applied data augmentation and normalization techniques to enhance model robustness.
   - Split the dataset into training and validation sets using `sklearn`.

3. **Model Training**:
   - Fine-tuned the YOLOv5 model on the custom dataset.
   - Used 5-fold cross-validation to optimize hyperparameters and prevent overfitting.

4. **Evaluation**:
   - Evaluated the model on the validation set to achieve a mAP of 0.85 and AP of 0.92.

5. **Deployment**:
   - Deployed the model for real-time detection with an average inference time of 0.5 seconds.

## How to Run the Project
1. Clone this repository:
   ```bash
   git clone https://github.com/ultralytics/yolov5.git
   cd yolov5
   pip install -r requirements.txt

    Download the dataset and place it in the specified directory.
    Train the model using the command:

python train.py --img 640 --batch 16 --epochs 50 --data dataset.yaml --weights yolov5s.pt

Evaluate the model:

python val.py --data dataset.yaml --weights best.pt

Run inference:

    python detect.py --source /path/to/images_or_video --weights best.pt --img 640

Results

    Performance Metrics:
        mAP: 0.85
        AP: 0.92
    Inference Speed: Average inference time of 0.5 seconds per image.

This is the output.

    ![Screenshot (254)](https://github.com/user-attachments/assets/d1053af9-03ae-4cf7-927a-008a9b52ab7e)


Future Work

    Extend the model to detect other lunar features.
    Optimize the model for deployment on low-power devices.

Acknowledgments

Special thanks to Ultralytics for the YOLOv5 framework and the open-source community for their support.

Feel free to contribute to this project or raise issues for further improvements.




