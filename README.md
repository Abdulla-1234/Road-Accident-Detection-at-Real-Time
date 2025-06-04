# Road Accident Detection and Alert System using Deep Learning 🚗

## Project Overview  
This project implements a **real-time road accident detection and alert system** using **deep learning techniques**. The system processes live or recorded **CCTV footage** to detect accidents using **Convolutional Neural Networks (CNNs)** and sends an **automated alert** via Telegram in case of an accident.  

## Abstract  
Traffic accidents are a major cause of fatalities worldwide, often due to **delayed emergency responses**. This project proposes an **AI-driven solution** that can:  
- Detect accidents in **real-time** using **CNN-based deep learning models**.  
- Send **immediate alerts** via **Telegram API**, containing time, location, and accident details.  
- Reduce **response time** for emergency services.  

The system is **trained on a subset of the UCF Crime Dataset** and fine-tuned with data augmentation to improve detection accuracy.  

## System Workflow  
Below is the **workflow diagram** of the accident detection and alert system: 

<img src="https://github.com/Abdulla-1234/Road-Accident-Detection-at-Real-Time/blob/main/Images/Workflow%20Diagram.png" alt="Workflow Diagram" width="400"/>

---

## Methodology  

### 1️⃣ Data Collection & Preprocessing  
- Dataset: **CCTV footage** with accident and non-accident frames.  
- Resized images to **250x250 pixels** and applied **data augmentation**.  

### 2️⃣ Model Selection & Training  
- Implemented a **custom sequential CNN model**.  
- Compared against **pretrained models**: GoogleNet, ResNet50, MobileNetV2, and Vision Transformers.  

### 3️⃣ Accident Detection Pipeline  
- Processes **video frames in real-time**.  
- Uses **CNN classification** to determine accident probability.

<img src="https://github.com/Abdulla-1234/Road-Accident-Detection-at-Real-Time/blob/main/Images/Accident%20Detection%20Pipeline.png" alt="Accident Detection Pipeline" width="400"/>

### 4️⃣ Alert System  
- If an accident is detected across **multiple frames**, an alert is generated.  
- Alert **sends an image**, timestamp, and location to a **Telegram group** using the **Telegram Bot API**.  

<img src="https://github.com/Abdulla-1234/Road-Accident-Detection-at-Real-Time/blob/main/Images/Alert%20Image.png" alt="Alert System" width="200"/> |

---

## Model Performance  

| Model               | Accuracy | Precision | Recall | F1-Score |
|---------------------|----------|-----------|--------|----------|
| **Sequential CNN**  | **95%**  | **92%**   | **95%** | **96%**  |
| EfficientNetB0      | 94%      | 94%       | 94%    | 93%      |
| GoogleNet          | 94%      | 94%       | 94%    | 94%      |
| ResNet50          | 93%      | 93%       | 93%    | 92%      |
| MobileNetV2       | 94%      | 93%       | 93%    | 93%      |
| Vision Transformer | 91%      | 91%       | 91%    | 91%      |


## Model Training Performance  
Below are the **training accuracy** and **loss graphs**:  

<div style="display: flex; justify-content: center;">
  <img src="https://github.com/Abdulla-1234/Road-Accident-Detection-at-Real-Time/blob/main/Images/Training%20accuracy%20and%20val_accuracy..png" alt="Training Accuracy" width="400"/>
  <img src="https://github.com/Abdulla-1234/Road-Accident-Detection-at-Real-Time/blob/main/Images/Training%20loss%20and%20val_loss..png" alt="Training Loss" width="400"/>
</div>

<p align="center">
  <em>Figure: Accuracy improvement over epochs (Left) & Loss reduction over epochs (Right).</em>
</p>

---

## Alert System Example  

Here’s an example of the **Telegram alert message** sent in case of an accident

