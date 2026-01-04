
# Oral Cancer Detection using DenseNet169 🧬

This project implements a **binary image classifier** to distinguish between **Cancerous** and **Non‑Cancerous** oral images using **DenseNet169** as the backbone. The notebook is designed to run on **Google Colab** and includes dataset preparation, model training, evaluation, and prediction with a simple upload widget.

---

## 📂 Project Structure
- **Module 1:** Install Dependencies  
- **Module 2:** Import Libraries  
- **Module 3:** Download & Extract Dataset  
- **Module 4:** Organize Dataset into Train/Test folders  
- **Module 5:** Train DenseNet169 Model  
- **Module 6:** Save & Download Model + Prediction Interface  

---

## ⚙️ Dependencies
The notebook installs and uses:
- `tensorflow`
- `numpy`
- `PIL`
- `ipywidgets`
- `requests`
- `shutil`, `os`, `zipfile`, `random`

---

## 📊 Dataset
- Source: [Elsevier Oral Cancer Dataset](https://prod-dcd-datasets-cache-zipfiles.s3.eu-west-1.amazonaws.com/mhjyrn35p4-2.zip)  
- Classes:  
  - **Benign → Non‑Cancer**  
  - **Malignant → Cancer**  
- The dataset is automatically downloaded and split into **train (80%)** and **test (20%)** sets.

---

## 🧠 Model Architecture
- **Base Model:** DenseNet169 (pretrained on ImageNet, frozen layers)  
- **Custom Layers:**  
  - Flatten  
  - Dense (128, ReLU)  
  - Dropout (0.5)  
  - Dense (1, Sigmoid)  

- **Loss Function:** Binary Crossentropy  
- **Optimizer:** Adam  
- **Metrics:** Accuracy  

---

## 🏋️ Training
- Image augmentation applied (rotation, zoom, flips, shifts).  
- Early stopping and model checkpoint callbacks included.  
- Trains for **10 epochs** with batch size **32**.  
- Best model saved as:  
  - `model/densenet169_binary_classifier.h5`  
  - Final model: `final_densenet169_model.h5`

---

## 🔍 Prediction
- Upload an image using the Colab widget.  
- Model outputs:  
  - **Label:** Cancerous / Non‑Cancerous  
  - **Confidence Score (%).**

---

## 🚀 How to Run
1. Open the notebook in **Google Colab**.  
2. Run all cells sequentially.  
3. Upload an oral image in the widget at the end.  
4. View prediction results instantly.

---

## 📈 Results
- The model achieves strong performance on the test set with DenseNet169 transfer learning.  
- Predictions include confidence scores for interpretability.

---

## 📌 Future Improvements
- Add Grad‑CAM visualization for explainability.  
- Extend dataset with more diverse oral cancer images.  
- Deploy as a web app using **Flask/Django + Angular frontend**.  
- Dockerize for reproducible builds.

---

## 🙌 Acknowledgements
- Dataset provided via Elsevier Data Repository.  
- TensorFlow/Keras for deep learning framework.  
- Google Colab for training environment.

---

## 👨‍💻 Author
**Inthiyaz**  
Final‑year B.Tech Computer Science student passionate about backend systems, AI integration, and recruiter‑friendly project deployment.
