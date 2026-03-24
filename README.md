# DeepFake Detection System

A deep learning pipeline to classify images as **Fake** (deepfake) or **Real**. The system compares a custom CNN baseline with three pretrained models (ResNet18, VGG16, Vision Transformer) and provides a live web interface for interactive predictions.

## 🚀 Live Demo

Try it yourself: [DeepFake Detector Playground](https://deepfake-detector-playground.lovable.app)

Upload an image and get an instant prediction with confidence score.

## 📁 Repository Contents

- `DeepFake_Detection.ipynb` – The main Jupyter notebook with data loading, preprocessing, training, and evaluation.
- `Explanation.pdf` – Detailed project report covering methodology, results, challenges, and deployment.
- `README.md` – This file.

## 🧠 Models Evaluated

| Model          | Type             | Best Val F1 | Best Val Acc |
|----------------|------------------|-------------|--------------|
| ResNet18       | Pretrained       | 0.9991      | 0.9991       |
| VGG16          | Pretrained       | 0.9981      | 0.9981       |
| Vision Transformer (ViT) | Pretrained | 0.9962      | 0.9961       |
| SmallCNN       | From scratch     | 0.9038      | 0.8926       |

All models were trained on the DeepFake vs Real 60k dataset using a two‑stage fine‑tuning strategy.

## 🛠️ How to Use

1. **Clone the repository**  
   ```bash
   git clone https://github.com/yourusername/deepfake-detection.git
   cd deepfake-detection