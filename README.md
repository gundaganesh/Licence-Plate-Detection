# License Plate Detection and Recognition Project

## Introduction  
This project focuses on **License Plate Detection and Recognition (LPDR)**, which involves two key tasks:  
1. **License Plate Detection** – Identifying and localizing license plates within vehicle images using object detection.  
2. **Character Recognition** – Extracting and recognizing alphanumeric characters from the detected plates.  

The project utilizes a custom dataset of vehicle images and leverages state-of-the-art deep learning models to achieve accurate detection and recognition. This solution can be applied to automated traffic monitoring and parking management systems.

---

## Data Collection and Preprocessing  
- The dataset contains approximately 350 images.  
- Preprocessing steps include:  
  - Resizing images to a fixed resolution of **640x640 pixels** for model compatibility.  
  - Applying **data augmentation** techniques, such as horizontal flips, to increase dataset size and diversity.

---

## Model Used  

### YOLOv8 (You Only Look Once, version 8)  
- A Convolutional Neural Network (CNN)-based architecture optimized for real-time object detection.  
- The model consists of:  
  - A **backbone** for feature extraction.  
  - A **detection head** that outputs bounding boxes around detected license plates.  
- Detection involves:  
  - A **sliding window approach** and convolution operations.  
  - **Non-max suppression** to select the most accurate bounding boxes.  

### EasyOCR  
- A Python-based **Optical Character Recognition (OCR)** library used for text extraction.  
- The OCR model uses **feature extraction** and **pattern matching** to accurately recognize characters from license plates.

---

## Training and Validation  
- The YOLOv8 model was trained on the dataset for **50 epochs** using pre-trained weights.  
- Performance metrics include:  
  - **Confusion Matrix**: Achieved 89% accuracy for license plate detection.  
  - **Loss Metrics**: Box loss, classification loss, and overall loss decreased steadily, indicating effective learning.  
  - **Precision**: Improved consistently across epochs, demonstrating increased prediction accuracy.

---

## Results  
- The model successfully detects license plates in images and recognizes characters using EasyOCR.  

### Testing Phase  
- **Images**: The model accurately identifies plates and extracts text from test images.  
- **Video**: Real-time detection and recognition were demonstrated on video input, showcasing the model’s robustness and efficiency.
