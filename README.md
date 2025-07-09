# 📦 MobileNet Lightweight Image Classification API

This project demonstrates a **lightweight image classification REST API** built using:

- 🧠 **MobileNetV2** (pretrained on ImageNet)
- ⚡ **FastAPI** for web service
- 🐳 **Docker** for containerization
- 🧪 Tested on a **NVIDIA T4 VM** during internship at **Cyborg Network**

---

## 📌 Project Objectives

- Build a minimal image classification API with low resource usage.
- Deploy the model using FastAPI and Docker.
- Run it on a lightweight GPU instance (NVIDIA T4).
- Provide external access for predictions and testing.

---

## 🧠 Model Details

- **Architecture**: MobileNetV2
- **Framework**: PyTorch (`torchvision.models`)
- **Pretrained on**: ImageNet (1000 classes)

---

## 🚀 How to Use

### 1. Clone the Repository

```bash
git clone https://github.com/nikunjgalaiya/mobilenet-lightweight-api.git
cd mobilenet-lightweight-api
2. Build Docker Image
bash
Copy code
docker build -t mobilenet-api .
3. Run the Docker Container
bash
Copy code
docker run -d -p 8000:8000 mobilenet-api
4. Test the API
Using Browser (Swagger Docs)
Open: http://localhost:8000/docs

Using cURL
bash
Copy code
curl -X POST "http://localhost:8000/predict/" \
  -H "accept: application/json" \
  -F "file=@your_image.jpg"
🧾 Project Files
bash
Copy code
mobilenet-lightweight-api/
├── app.py              # FastAPI application
├── Dockerfile          # Instructions to build image
├── requirements.txt    # Python dependencies
└── README.md           # Project overview and usage guide
🔧 app.py (API Overview)
Loads pretrained MobileNetV2

Accepts image uploads via /predict/ endpoint

Transforms image and returns predicted class name & ID

📦 requirements.txt
txt
Copy code
fastapi
uvicorn
torch
torchvision
Pillow
requests
Install locally with:

bash
Copy code
pip install -r requirements.txt
Run locally with:

bash
Copy code
uvicorn app:app --host 0.0.0.0 --port 8000
🧪 Testing
Successfully tested on:

✅ NVIDIA T4 VM (Azure NCas T4 v3)

✅ Port 8000 exposed via Docker

✅ Predictions returned using cURL and Swagger UI

👤 Author
Name: Nikunj Galaiya

GitHub: @nikunjgalaiya

Internship: Cyborg Network

Mentor: Barath (Project Coordinator)
