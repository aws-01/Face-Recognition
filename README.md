# 🎯 Facial Recognition Web App

An interactive facial recognition web application built with **Flask** and deployed using **Docker**.  
The app leverages **AWS Rekognition** to detect and identify faces, stores recognized users in **DynamoDB**, and provides an intuitive web interface for uploading and checking images.

---

## 🚀 Features

- 📸 **Image Upload** – Upload images via web interface  
- 🔍 **Face Detection & Recognition** – Detect and identify faces using AWS Rekognition  
- 🗄️ **DynamoDB Storage** – Store recognized faces in `cricketers_data`  
- 🐳 **Dockerized Deployment** – Run Flask app easily with Docker  
- 💻 **Responsive Design** – Works on desktop, tablet, and mobile  
- ☁️ **AWS Integration** – Uses S3, Rekognition, DynamoDB, and Lambda for automation  

---

## 🧰 Technologies Used

| Category       | Technology                                   |
|----------------|---------------------------------------------|
| Backend        | Python 3.10, Flask                           |
| Frontend       | HTML, CSS, JavaScript                        |
| Image Handling | Pillow                                       |
| Cloud Services | AWS Rekognition, AWS S3, AWS DynamoDB, AWS Lambda |
| Containerization | Docker                                     |
| Version Control | Git & GitHub                                |

---

## ☁️ AWS Architecture Overview

### 🧩 **Amazon S3**
- Stores uploaded images in a bucket (e.g., `cricketers-images001`).  
- Each image has metadata `FullName` to store the cricketer’s name.  

### 🔍 **AWS Rekognition**
- Detects and identifies faces in images.  
- Maintains a face collection called `cricketers`.  

### 🗄️ **Amazon DynamoDB**
- Stores recognized face IDs and full names in the table `cricketers_data`.  
- DynamoDB is automatically updated via **Lambda** when new images are uploaded to S3.  

### ⚙️ **AWS Lambda**
- Triggered on new image uploads to S3.  
- Indexes faces into Rekognition and updates DynamoDB automatically.  

---

## 📂 Project Structure
