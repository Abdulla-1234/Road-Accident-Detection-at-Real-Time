# 🚗 Road Accident Detection and Alert System using Deep Learning  

## 📌 Project Overview  
This project implements a **real-time road accident detection and alert system** using **deep learning techniques**. The system processes live or recorded **CCTV footage** to detect accidents using **Convolutional Neural Networks (CNNs)** and sends an **automated alert** via Telegram in case of an accident.  

## 🔍 Abstract  
Traffic accidents are a major cause of fatalities worldwide, often due to **delayed emergency responses**. This project proposes an **AI-driven solution** that can:  
- Detect accidents in **real-time** using **CNN-based deep learning models**.  
- Send **immediate alerts** via **Telegram API**, containing time, location, and accident details.  
- Reduce **response time** for emergency services.  

The system is **trained on a subset of the UCF Crime Dataset** and fine-tuned with data augmentation to improve detection accuracy.  

## 📷 System Workflow  
Below is the **workflow diagram** of the accident detection and alert system:  

![Workflow Diagram](images/workflow.png)  

---

## 🏗️ Methodology  

### 1️⃣ Data Collection & Preprocessing  
- Dataset: **CCTV footage** with accident and non-accident frames.  
- Resized images to **250x250 pixels** and applied **data augmentation**.  

### 2️⃣ Model Selection & Training  
- Implemented a **custom sequential CNN model**.  
- Compared against **pretrained models**: GoogleNet, ResNet50, MobileNetV2, and Vision Transformers.  

### 3️⃣ Accident Detection Pipeline  
- Processes **video frames in real-time**.  
- Uses **CNN classification** to determine accident probability.  

![CNN Model Architecture](images/cnn_model.png)  

### 4️⃣ Alert System  
- If an accident is detected across **multiple frames**, an alert is generated.  
- Alert **sends an image**, timestamp, and location to a **Telegram group** using the **Telegram Bot API**.  

![Alert System](images/alert_system.png)  

---

## 📊 Model Performance  

| Model               | Accuracy | Precision | Recall | F1-Score |
|---------------------|----------|-----------|--------|----------|
| **Sequential CNN**  | **95%**  | **92%**   | **95%** | **96%**  |
| EfficientNetB0      | 94%      | 94%       | 94%    | 93%      |
| GoogleNet          | 94%      | 94%       | 94%    | 94%      |
| ResNet50          | 93%      | 93%       | 93%    | 92%      |
| MobileNetV2       | 94%      | 93%       | 93%    | 93%      |
| Vision Transformer | 91%      | 91%       | 91%    | 91%      |

### 📊 Model Training Performance  
Below are the **training accuracy** and **loss graphs**:  

![Training Accuracy](images/training_accuracy.png)  
*Figure: Accuracy improvement over epochs.*  

![Training Loss](images/training_loss.png)  
*Figure: Loss reduction over epochs.*  

---

## 📢 Alert System Example  

Here’s an example of the **Telegram alert message** sent in case of an accident:  

