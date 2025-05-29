# Caltech101-ResNet18-FineTuning# Caltech-101 Image Classification with Fine-tuned ResNet-18

This project implements an image classification model for the Caltech-101 dataset using a fine-tuned ResNet-18 architecture pretrained on ImageNet. The project demonstrates the power of transfer learning for small-scale image classification tasks.

## 📂 Project Structure

Caltech101-ResNet18-FineTuning/
├── data/ # Caltech-101 dataset directory
├── models/ # Trained model weights
├── plots/ # Training curves and visualizations
├── train.py # Main training script
├── predict.py # Prediction script
├── requirements.txt # Python dependencies
└── README.md # Project description


## 🗂 Dataset

- **Caltech-101**: [Download Link](https://data.caltech.edu/records/mzrjq-6wc02)
- Contains 101 categories + 1 background class (~9144 images).
- Images resized to 224×224 and normalized using ImageNet mean/std.

## 🏗️ Model Details

- **Architecture**: ResNet-18 (pretrained on ImageNet).
- **Fine-tuning**: Last fully connected layer replaced for 101-class classification.
- **Optimizer**: Adam, learning rate = 0.0001.
- **Loss**: CrossEntropyLoss.
- **Epochs**: 10.
- **Batch Size**: 32.
- **Accuracy**: Achieved ~97% validation accuracy.

## 📊 Results

| Epoch | Train Loss | Train Accuracy | Val Loss | Val Accuracy |
|:----|:------------|:---------------|:---------|:-------------|
| 1    | 1.6848     | 0.6852         | 0.5846   | 0.9124       |
| 5    | 0.0201     | 0.9996         | 0.1678   | 0.9700       |
| 10   | 0.0049     | 0.9997         | 0.1522   | 0.9683       |

## 🔍 How to Run

### 1️⃣ Clone the repository
git clone https://github.com/your-username/Caltech101-ResNet18-FineTuning.git
cd Caltech101-ResNet18-FineTuning
### 2️⃣ Install dependencies
pip install -r requirements.txt
### 3️⃣ Download the dataset
Download and extract the Caltech-101 dataset into the data/ directory.
### 4️⃣ Train the model
python train.py
### 5️⃣ Predict on a single image
python predict.py --image_path ./data/airplanes/image_0001.jpg
