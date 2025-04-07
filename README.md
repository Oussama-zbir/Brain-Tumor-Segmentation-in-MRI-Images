# Brain Tumor Segmentation in MRI Images

A deep learning project for brain tumor detection and segmentation in MRI images, built with TensorFlow and Keras.

## Overview
This project focuses on brain tumor detection and segmentation in MRI scans using deep learning approaches:
1. Classification models (ResNet50, VGG16) to detect the presence of tumors
2. Segmentation model (ResUNet) to precisely locate and outline tumor regions

## Dataset
The project uses the LGG MRI Segmentation dataset from Kaggle which contains brain MRI images together with manual FLAIR abnormality segmentation masks. The dataset includes:
- 3929 brain MRI images (2556 without tumors, 1373 with tumors)
- Corresponding segmentation masks for tumor regions

## Features
- Data preprocessing and exploratory analysis
- Data augmentation with ImageDataGenerator
- Transfer learning with ResNet50 and VGG16 for classification
- Custom ResUNet implementation for segmentation
- Custom loss functions (Tversky, Focal Tversky) for handling class imbalance
- Comprehensive visualization of results

## Models
1. **Classification**:
   - ResNet50 (pretrained on ImageNet): 60% accuracy
   - VGG16 (pretrained on ImageNet): 50% accuracy

2. **Segmentation**:
   - ResUNet with custom Tversky loss function

## Requirements
See requirements.txt file for dependencies.

## Usage
1. Clone the repository
2. Install the dependencies: `pip install -r requirements.txt`
3. Download the LGG MRI dataset from Kaggle
4. Run the notebook to train and evaluate the models

## Model Weights
Pre-trained weights are available in the repository:
- `clf-resnet-weights.hdf5`: ResNet50 classification model
- `vgg16_1.h5`: VGG16 classification model
- `ResUNet-segModel-weights.hdf5`: ResUNet segmentation model

## Results
- ResNet50 classification: 60% accuracy
- VGG16 classification: 50% accuracy
- ResUNet segmentation: Visualized with colored overlays on MRI scans

## License
MIT
