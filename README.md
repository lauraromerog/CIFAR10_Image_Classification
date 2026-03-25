# CIFAR-10 Image Classification: Custom CNN vs. Transfer Learning

## Project Overview
This project explores the performance gap between a Convolutional Neural Network (CNN) built from scratch and modern Transfer Learning architectures (MobileNetV2, EfficientNetB0, and ResNet50V2) using the CIFAR-10 dataset.

## Key Findings
* **Custom CNN:** Achieved ~74% accuracy but required significant manual tuning and longer training times.
* **Transfer Learning:** MobileNetV2 emerged as the most efficient model, reaching 80%+ accuracy almost instantly.
* **Optimization:** Used Data Augmentation, Batch Normalization, and Fine-Tuning to maximize performance.

## How to Run
1. Install dependencies: `pip install -r requirements.txt`
2. Open the Jupyter Notebook/VS Code and run all cells.
3. The script will automatically train the models, compare results, and save the best performing model as a `.keras` file.

## Results
The project includes a final benchmarking suite that visualizes Accuracy and Loss curves across all tested architectures.
