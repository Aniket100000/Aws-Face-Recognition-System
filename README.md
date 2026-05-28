![AWS](https://img.shields.io/badge/AWS-Rekognition-orange)
![Python](https://img.shields.io/badge/Python-3.x-blue)
![Flask](https://img.shields.io/badge/Flask-Backend-black)
![EC2](https://img.shields.io/badge/AWS-EC2-yellow)
![S3](https://img.shields.io/badge/AWS-S3-red)
![Status](https://img.shields.io/badge/Status-Active-success)


🚀 FaceID Cloud – Intelligent Face Recognition System 

A complete cloud-based face recognition system built using AWS Rekognition, supporting both:

🧪 Serverless CLI-based workflow (S3 + CloudShell)
🌐 Full-stack Web App (Flask + EC2 + Modern UI)

🌐 Live Demo (Web App)

👉 http://13.233.45.217:5000

⚠️ Demo server may be temporarily offline when EC2 instance is stopped to optimize AWS Free Tier usage.


📌 Project Overview

This project demonstrates how to build a real-world AI-powered face recognition system using AWS services.

It was developed in two phases:

🔹 Phase 1: Serverless (AWS CLI + S3)

Face recognition using AWS Rekognition + S3
No backend server required
Executed via AWS CloudShell

🔹 Phase 2: Full Stack Web App

Interactive UI built with modern frontend
Backend using Flask (Python)
Deployed on AWS EC2
Real-time face upload and matching


✨ Features

🔍 Real-time face detection and recognition

🤖 AWS Rekognition powered AI matching

⚡ Fast response time (<2 seconds)

🎯 High accuracy face comparison

☁️ Cloud deployment on AWS EC2

🗂️ Image storage using Amazon S3

🔐 IAM Role-based secure authentication

🌐 Modern Flask web application

📸 Drag-and-drop image upload UI

🧠 Face collection-based recognition system

💻 Supports both CLI and Web workflows


🔹 Frontend

HTML5
CSS3 (Modern UI Design)
JavaScript

🔹 Backend (Phase 2)

Flask (Python)
Boto3 (AWS SDK)

🔹 Cloud Services

AWS Rekognition (Face Detection & Matching)
Amazon S3 (Image Storage)
AWS EC2 (Hosting)
AWS IAM (Security & Access Control)
AWS CloudShell (CLI Execution)




🏗️ Architecture


User Browser
      ↓
Flask App (AWS EC2)
      ↓
AWS Rekognition
      ↓
AWS S3 Storage

IAM Role → EC2





⚙️ How It Works

🔹 Phase 1 – Serverless Workflow

1.User uploads image to Amazon S3

2.AWS Rekognition indexes the face

3.Face collection stores embeddings

4.Rekognition searches for matches

5.Confidence score returned


🔹 Phase 2 – Web Application Workflow

1.User uploads image from browser

2.Flask backend receives image

3.Image sent to AWS Rekognition

4.Rekognition compares face with collection

5.Result displayed with confidence score


🔹 AWS Services Used

1.Amazon Rekognition → Face Detection & Matching

2.Amazon S3 → Image Storage

3.AWS EC2 → Hosting Flask Application

4.AWS IAM → Security & Permissions

5.AWS CloudShell → CLI Workflow



📸 Screenshots

🔹  AWS EC2 Terminal




🔹 Face - Indexed




🔹Face Recognition Result




🔹 Face Recognition Terminal




🔹 Homepage UI




🔹 AWS S3 Storage




⚙️ Steps Performed (Phase 1 – CLI)

1️⃣ Configure AWS
aws configure set region ap-south-1

2️⃣ Create Collection
aws rekognition create-collection \
  --collection-id free-face-collection

3️⃣ Upload Image to S3
Bucket: face-recognition-free-test
Path: test/person1.jpeg

4️⃣ Index Face
aws rekognition index-faces \
  --collection-id free-face-collection \
  --image "S3Object={Bucket=face-recognition-free-test,Name=test/person1.jpeg}" \
  --external-image-id "person1"

 ☁️ AWS EC2 Deployment


python app.py


* Hosted on AWS EC2
* IAM Role attached for secure AWS access
* AWS Rekognition used for face matching
* AWS S3 used for image storage

  
🌐 How Web App Works (Phase 2)

User uploads image from browser

Flask backend receives file

Image sent to AWS Rekognition

Faces matched with collection

Result shown with confidence score




📊 Example Output

✅ Match Found
🎯 Confidence: 100%
🧑 Person ID: person1


📂 Project Structure

face-recognition-aws/
│
├── app.py
├── templates/
├── static/
├── screenshots/
├── commands/
│   └── rekognition-commands.txt
└── README.md


🖥️ Tech Stack

⚙️ Installation & Setup

Clone the repository:

git clone https://github.com/Aniket100000/Aws-Face-Recognition-System.git

Go to project folder:

cd Aws-Face-Recognition-System

Install dependencies:

pip install -r requirements.txt

Run Flask app:

python app.py




🔐 Security

IAM roles used (no hardcoded credentials)

Secure API access to Rekognition

Follows best practices




💰 Cost Consideration

Built using AWS Free Tier

Minimal resource usage

Optimized API calls




🎯 Key Learnings

AWS Rekognition hands-on implementation

Serverless architecture (S3 + CLI)

Full-stack deployment on EC2

Integration of AI with web apps

Real-world cloud project building


🔮 Future Enhancements

🔐 User authentication system

📸 Real-time webcam face recognition

📱 Fully responsive mobile UI

🔒 HTTPS/SSL deployment

🗄️ Store recognition results in DynamoDB

☁️ Deploy using Docker & Kubernetes

🎥 Live video recognition using Rekognition Video API

🌍 Custom domain integration

📊 CloudWatch monitoring dashboard

⚡ Serverless migration using AWS Lambda

👨‍💻 Author
Aniket Kushwaha
📧 Aniketkushwaha10064@gmail.com
📱 9736550069
