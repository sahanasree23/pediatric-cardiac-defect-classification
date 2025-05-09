# Pediatric Cardiac Defect Classification

This project implements a deep learning pipeline for classifying pediatric congenital heart defects (CHDs) such as ASD, VSD, PDA, and Normal from radiographic images. It integrates Graph Cut segmentation with deep residual networks (ResNet-50 and ResNet-152) for improved accuracy.

## 🧠 Model Overview

- **Models Used**:
  - ResNet-50
  - ResNet-50 + Graph Cuts
  - ResNet-152
  - ResNet-152 + Graph Cuts (best performance)

- **Segmentation Technique**: GrabCut (Graph Cut) with morphological operations

## 📊 Evaluation Metrics

| Model                  | Accuracy | Precision | Recall | F1 Score | Cohen's Kappa | MCC   |
|------------------------|----------|-----------|--------|----------|---------------|-------|
| ResNet-50             | 0.8072   | 0.8132    | 0.8072 | 0.8089   | 0.7376        | 0.7386|
| ResNet-50 + GraphCuts | 0.8921   | 0.8924    | 0.8921 | 0.8914   | 0.8529        | 0.8534|
| ResNet-152            | 0.8296   | 0.8339    | 0.8296 | 0.8272   | 0.7682        | 0.7704|
| ResNet-152 + GraphCuts| 0.9198   | 0.9222    | 0.9198 | 0.9203   | 0.8913        | 0.8918|

## 🧪 Dataset

- 828 pediatric X-ray images
- Augmented to 6485 images using rotation, flipping, brightness/contrast adjustments
- Classes: `ASD`, `PDA`, `VSD`, `Normal`

## ⚙️ Tech Stack

- Python
- PyTorch
- OpenCV
- Google Colab

## 📂 Project Structure
├── data/
│ ├── ASD/
│ ├── PDA/
│ ├── VSD/
│ └── Normal/
├── segmentation/
│ └── graph_cut.py
├── models/
│ └── resnet152_model.py
├── training/
│ └── train.py
├── evaluation/
│ └── confusion_matrix.png
├── plots/
│ ├── accuracy_plot.png
│ └── loss_plot.png
├── README.md


## 📌 Results

- Confusion matrices
- Accuracy/Loss graphs
- Notable improvement with Graph Cut segmentation

## 🚀 Future Work

- Add a testing phase with unseen data
- Integrate with real-time diagnostic tools
- Extend to other imaging modalities (e.g., CT or MRI)

## 📸 Sample Output

*(Insert sample segmented image and classification result here)*

---

Let me know if you'd like me to help generate a sample `README.md`, a `.gitignore` file, or a `requirements.txt`.

