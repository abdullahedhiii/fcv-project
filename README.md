# Simplified SILCO: One-Shot Semantic Segmentation

This repository contains the implementation of a simplified SILCO (Spatial-Interactive Learning with Conditional features) architecture for One-Shot Semantic Segmentation, developed for the Fundamentals of Computer Vision course.

## Project Structure
- **Dataset**: Pascal VOC 2007.
- **Backbone**: ResNet-50.
- **Core Module**: Similarity Guidance Module (SGM) for dense spatial matching.
- **Evaluation**: Mean Intersection over Union (mIoU) and Pixel Accuracy.

## Environment Setup
- Python 3.10+
- PyTorch 2.0+
- Torchvision
- Matplotlib, Numpy

## How to Run

### 1. Training
The training script utilizes episodic sampling. To start training:
- Ensure the `data` directory contains the Pascal VOC files.
- Run the training block. It will automatically save checkpoints in `/checkpoints/latest.pth`.
- The script includes a safe loading mechanism; if a checkpoint exists but the architecture has changed, it will default to a fresh training session.

### 2. Evaluation
To evaluate the trained model:
- Load the `best.pth` checkpoint.
- The `evaluate_model` function runs 500 episodes to generate the final mIoU and Accuracy scores.

### 3. Inference & Visualization
The final cell in the notebook provides a qualitative visualization grid. It displays:
1. Support Image/Mask 
2. Query Image 
3. Ground Truth vs. SILCO Prediction Heatmap

## Authors
- Abdullah Anis Edhi (22K-4392)
- Muhammad Taha Khan (22K-4609)
