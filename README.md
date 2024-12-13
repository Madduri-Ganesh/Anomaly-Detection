# Anomaly Detection in Medical Images using Patchcore

## Overview
This project implements an **anomaly detection** system for medical images, specifically chest X-rays, using the **Anomalib** library. The model is based on the **Patchcore** architecture with a pre-trained **ResNet50** backbone, designed to identify abnormalities in chest X-ray images.

## Model Architecture
- **Base Model**: Patchcore
- **Backbone**: ResNet50 (pre-trained)
- **Input Size**: 64x64 pixels
- **Feature Extraction**: 100 features from ResNet50 layers ('layer1', 'layer2', 'layer3')
- **Library**: Anomalib

## Dataset
- **Normal Images**: Chest X-rays in PNG format
- **Abnormal Images**: Left-right flipped versions of normal images in TIF format
- **Image Size**: 256x256 pixels
- **Dataset Structure**: Implemented using Anomalib's `Folder` class

## Data Preprocessing
- **Resizing** of images to 256x256 pixels
- **Further resizing** to 64x64 pixels for model input

## Training Details
- **Task**: Classification
- **Engine**: Anomalib's `Engine` class
- **Batch Size**: 32
- **Data Loading**: 2 worker threads

## Model Configuration
- **Input Size**: 64x64 pixels
- **Feature Extraction**:
  - **Layers**: 'layer1', 'layer2', 'layer3' of ResNet50
  - **Features**: 100 from each layer
