🧠 AI vs Real – Image Authenticity Detection Chrome Extension

AI vs Real is a Chrome browser extension that detects whether an image is AI-generated or real using a deep learning model (ResNet50) served via a Python Flask backend.
The extension enables users to analyze images directly from the web in real time, helping combat misinformation and synthetic media misuse.

🚀 Features

🔍 Detects AI-generated vs real images

🌐 Works directly inside the Chrome browser

⚡ Real-time prediction using a Flask REST API

🧠 Deep learning–based image classification (ResNet50)

🎨 Clean and simple popup UI

🔒 Local backend for privacy and control

🏗️ System Architecture
Chrome Extension (Frontend)
│
├── Popup UI (HTML, CSS, JS)
├── Content Script (Extracts images)
├── Background Script
│
▼
Flask Backend (Python)
│
├── REST API
├── Image Preprocessing
├── ResNet50 Model (.pth)
│
▼
Prediction Output (AI / Real)

🛠️ Tools & Technologies Used
Frontend (Chrome Extension)

HTML5

CSS3

JavaScript (Vanilla JS)

Chrome Extension APIs

Manifest V3

Backend

Python 3.10+

Flask

Flask-CORS

Machine Learning

PyTorch

ResNet50 (pre-trained & fine-tuned)

OpenCV

NumPy

Pillow (PIL)

📁 Project Structure
AI vs Real Extension/
│
├── Extension_10-final/
│   ├── manifest.json
│   ├── background.js
│   ├── content_script.js
│   ├── popup.html
│   ├── popup.css
│   ├── popup.js
│   ├── icons/
│   │   ├── icon16.png
│   │   ├── icon48.png
│   │   └── icon128.png
│
├── backend/
│   ├── app.py
│   ├── requirements.txt
│   ├── models/
│   │   └── classifier_resnet50.pth
│   └── .venv/   (not recommended for GitHub)
│
└── README.md

⚙️ Setup & Installation
1️⃣ Backend Setup (Flask API)
cd backend
python -m venv venv
venv\Scripts\activate   # Windows
pip install -r requirements.txt
python app.py


➡️ Backend runs at: http://127.0.0.1:5000

2️⃣ Load Chrome Extension

Open Chrome → chrome://extensions

Enable Developer Mode

Click Load unpacked

Select the Extension_10-final folder

Extension is now active 🎉

🔄 How It Works

User opens the extension popup

Image URL is captured from the webpage

Image is sent to Flask API

Backend preprocesses the image

ResNet50 model predicts AI or Real

Result is returned and displayed in UI

📊 Model Details

Architecture: ResNet50

Framework: PyTorch

Input: RGB Image

Output: Binary Classification (AI / Real)

Model File: classifier_resnet50.pth

🔐 Privacy Considerations

No data is stored permanently

Images are processed only for prediction

Runs locally on user’s system

🚧 Limitations

Accuracy depends on dataset quality

Requires backend to be running

Limited to image-based detection (no video yet)

🌱 Future Enhancements

🔄 Online deployment (Cloud API)

🎥 Video deepfake detection

📈 Confidence score visualization

🧠 Multi-model ensemble

🌍 Firefox extension support

👨‍💻 Author

Anam Fatima, Aftab Alam, Arjita Sahu

📜 License

This project is licensed under the MIT License – feel free to use and modify.

⭐ If you like this project, don’t forget to star the repository!
