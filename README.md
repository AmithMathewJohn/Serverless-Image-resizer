# 🖼️ Serverless Image Resizer

A fully serverless image resizing web application built on 
Amazon Web Services (AWS) as part of a 30-Day Cloud Computing Bootcamp.

## 🌐 Live Demo
🔗 https://d2csuiorezdg89.cloudfront.net

## 👥 Team
- Amith Mathew John
- Ancy Vaz

## 🛠️ Tech Stack
| Service | Purpose |
|---------|---------|
| AWS Lambda | Serverless compute — image resizing |
| Amazon S3 | Storage for images and website hosting |
| AWS API Gateway | REST API for presigned URL generation |
| Amazon CloudFront | CDN and HTTPS secure delivery |
| Python 3.11 + Pillow | Image processing library |
| HTML / CSS / JavaScript | Frontend interface |

## ⚡ Features
- ✅ Upload images up to 5GB (Ultra HD supported)
- ✅ Custom resize dimensions (any width x height)
- ✅ Quick preset sizes (100x100 to 1920x1080)
- ✅ Auto orientation correction using EXIF data
- ✅ Real-time upload progress bar
- ✅ Secure HTTPS delivery via CloudFront
- ✅ Fully serverless — zero server management
- ✅ Pay only when used — extremely cost efficient

## 🏗️ Architecture
User Browser (HTTPS)
↓
Amazon CloudFront (SSL/TLS)
↓
S3 Website Bucket (Frontend)
↓
API Gateway → Lambda (Presigned URL Generator)
↓
Browser → S3 Input Bucket (Direct Upload)
↓
S3 Trigger → Lambda (Image Resizer)
↓
S3 Output Bucket (Resized Image)
↓
Browser displays resized image ✅

## 📁 Project Structure
serverless-image-resizer/
│
├── README.md
├── frontend/
│   └── index.html
├── lambda/
│   ├── ImageResizerFunction.py
│   └── GeneratePresignedURL.py
└── docs/
└── architecture.md

## 🚀 How It Works
1. User opens website via CloudFront HTTPS URL
2. User selects an image and desired dimensions
3. Frontend requests a presigned URL from API Gateway
4. Lambda generates a secure temporary S3 upload URL
5. Browser uploads image directly to S3 (up to 5GB!)
6. S3 automatically triggers the Image Resizer Lambda
7. Lambda resizes the image using Python Pillow
8. Resized image is saved to the output S3 bucket
9. Frontend displays the resized image with download option

## 💰 Cost
This project runs almost entirely within the AWS Free Tier.
Estimated cost for moderate usage — less than ₹20/month!

## 📅 Duration
30-Day Cloud Computing Bootcamp — 2026
