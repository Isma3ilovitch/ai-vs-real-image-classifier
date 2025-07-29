# AI vs Real Image Classifier 🧠📷

This project is a deep learning model that classifies whether an image is **AI-generated** or **real**, using a CNN with transfer learning (ResNet50).  
It uses the Kaggle dataset: [AI-Generated Images vs Real Images](https://www.kaggle.com/datasets/cashbowman/ai-generated-images-vs-real-images).

---

## 📁 Dataset

- Two classes:
  - `ai/` – AI-generated images
  - `real/` – Real photographs
- Used TensorFlow's `ImageDataGenerator` to preprocess, augment, and split the dataset into `train`, `val`, and `test`.

---

## 🧠 Model Architecture

- **Base Model**: ResNet50 (pre-trained on ImageNet, frozen)
- **Head**:
  - GlobalAveragePooling2D
  - Dense + Dropout
  - Output: Sigmoid (binary)

---

## 🏋️ Training

- Optimizer: Adam
- Loss: Binary Crossentropy
- Metrics: Accuracy
- Early stopping + checkpoint callbacks used

---

## 📊 Results

- Accuracy improved over training
- Evaluated with test set, confusion matrix, and visual predictions

---

## 🧪 How to Run

```bash
pip install -r requirements.txt
