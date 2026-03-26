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
- The Winner: MobileNetV2 achieved the highest accuracy at 86.17%. It is the most efficient choice for edge deployment due to its lightweight architecture. 
- The Runner-Up: EfficientNetB0 followed closely at 86.14%. Proving its "Compound Scaling" is highly effective even for smaller images.
- Custom CNN Performance: The scratch-built model hit 72.47 %. While a strong baseline, it reached a plateau where the animal classes (cats/dogs) became difficult to distinguish without pre-trained features.

## Ensamble 
The two best models are ensambled in a Soft Voting system. Instead of just looking at the final answer (e.g., "It's a Dog"), might be better to look at the raw probabilities (e.g., "I am 90% sure it's a Dog, and 10% sure it's a Cat").

It works by **asking the top models (EfficientNet and MobileNet) to predict the probabilities for the test images, calculating the average among those probabilities together, and picking the class with the highest average score.**

As the models make different types of mistakes, seems like a good enough approach to improve accuracy. If EfficientNet gets confused by a weirdly shaped car, MobileNet might recognize the wheels and "outvote" the mistake.

## How to Run
1. Install dependencies: `pip install -r requirements.txt`
2. Open the Jupyter Notebook/VS Code and run all cells.
3. The script will automatically train the models, compare results, and save the best performing model as a `.keras` file.

## Results
The project includes a final benchmarking suite that visualizes Accuracy and Loss curves across all tested architectures.

