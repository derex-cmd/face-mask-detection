# 😷 Face Mask Detection Using Deep Learning

A real-time deep learning system for detecting face mask compliance using webcam or video stream. Trained on over 4,000 labeled faces, the app classifies individuals as:
- ✅ With Mask
- ❌ Without Mask
- ⚠️ Mask Worn Incorrectly

Deployed using Flask with Haar Cascade for face detection and MobileNetV2 for classification.

---

## 📁 Dataset

- **Images:** 853
- **Annotated Faces:** 4,072
- **Labels:** `with_mask`, `without_mask`, `mask_weared_incorrect`
- **Split:** 70% Train, 15% Val, 15% Test
- **Preprocessing:** Face cropping, flipping, rotation, resizing (224x224), normalization.

---

## 🧠 Models Tested

- MobileNetV2 (✅ Best - Feature Extraction)
- MobileNetV2 (Fine-tuned)
- ResNet50 (Feature + Finetune)
- EfficientNetB0 (Feature + Finetune)

**Training:**  
- Optimizer: Adam  
- Loss: Categorical Cross-Entropy  
- Batch Size: 32  
- Epochs: 20  

---

## 🔍 Face Detection

- Haar Cascade (frontalface_default.xml) used to detect and crop face regions in real-time.

---

## 🌐 Deployment

- **App:** Flask
- **Video Feed:** Streamed at `http://127.0.0.1:5000`
- **Webcam Handling:** Robust fallback across indices 0–2 and test video if all fail
- **Bounding Box Colors:**  
  - 🟢 Green: With Mask  
  - 🔴 Red: Without Mask / Incorrect

---

## 📊 Evaluation

Evaluation is performed using accuracy, precision, recall, and F1-score.  

**Top Model: MobileNetV2 (Feature Extraction)**  
- Accuracy: **87.73%**
- F1 (With Mask): **0.9284**
- F1 (Without Mask): **0.7149**
- F1 (Mask Incorrect): **0.2609** ← class imbalance

---

## ✅ To Do

- [x] Build MobileNetV2/ResNet50 classifiers  
- [x] Real-time face detection via Haar  
- [x] Evaluate with F1, Precision, Recall  
- [ ] Add attention or MTCNN  
- [ ] Handle class imbalance  
- [ ] Expand dataset

---

## 🛠️ Requirements

| Library     | Version     |
|-------------|-------------|
| TensorFlow  | 2.17.0      |
| OpenCV      | 4.11.0      |
| NumPy       | Latest      |
| Flask       | Latest      |

---

## 📦 Installation

Clone the repo and install dependencies:

git clone https://github.com/derex-cmd/face-mask-detection.git
cd face-mask-detection
pip install -r requirements.txt


---

## ▶️ Run the App

python app.py

Then open your browser at: `http://127.0.0.1:5000`

---

## 🤝 Contributing

Feel free to fork this repo and submit pull requests.  
For major changes, open an issue first.

---

## 📜 License

This project is licensed under the **MIT License**.

---

## 🙋 Contact

**Developed by:** [Omer Nasir](https://github.com/derex-cmd) & [Ahad](https://github.com/ahad-must)  
Reach out via GitHub or LinkedIn for collaboration or questions.

