# CIFAR-10 Image Classification: Custom CNN vs. Transfer Learning

## Project Overview
This project explores the performance gap between a Convolutional Neural Network (CNN) built from scratch and modern Transfer Learning architectures (MobileNetV2, EfficientNetB0, and ResNet50V2) using the CIFAR-10 dataset.

## Enviroment
- **Hardware**: Trained on Google Colab using a T4 GPU.
- **Framework**: TensorFlow / Keras.

## Project Structure

```
CIFAR10_Image_Classification/
├── CIFAR10_Image_Classification.ipynb
├── requirements.txt
├── CIFAR10_Image_Classification_Findings.ppt
└── README.md
```

## Key Findings
- The Winner: EfficientNetB0 achieved the highest accuracy at 86.24%, proving its "Compound Scaling" is highly effective even for smaller images.
- The Runner-Up: MobileNetV2 followed closely at 85.91%. It is the most efficient choice for edge deployment due to its lightweight architecture.
- Custom CNN Performance: Our scratch-built model hit 76.03%. While a strong baseline, it reached a plateau where the animal classes (cats/dogs) became difficult to distinguish without pre-trained features.

## How to Run
1. Install dependencies: `pip install -r requirements.txt`
2. Open the Jupyter Notebook/VS Code and run all cells.
3. The script will automatically train the models, compare results, and save the best performing model as a `.keras` file.

## Results
The project includes a final benchmarking suite that visualizes Accuracy and Loss curves across all tested architectures.

