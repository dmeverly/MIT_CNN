# MIT-BIH ECG Heartbeat Classification with Residual 1D CNN

**Author**: David Everly  
**Language**: Python  
**Version**: 1  

### <a href="https://www.dmeverly.com/completedprojects/MIT_CNN/" style="display: block; text-align:right;" target = "_blank">  Project Overview -> </a>  
---  

## Description  

This project implements a deep learning CNN pipeline to classify cardiac arrhythmia types from single-lead (II) ECG waveforms in the MIT-BIH Arrhythmia dataset. The model is a custom 1D Residual Convolutional Neural Network (ResNet) trained on the Kaggle-formatted MIT-BIH dataset with 5 heartbeat classes. Key features include weighted sampling, Focal Loss to address class imbalance, and kernel/saliency map visualizations for interpretability.

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Features](#features)
- [Configuration](#configuration)
- [Examples](#examples)
- [Future Work and Extension](#future-work-and-extension)
- [References](#references)
- [Contributing](#contributing)
- [Licenses](#licenses)

## Installation  
Dependencies:  
- torch  
- numpy  
- pandas  
- matplotlib  
- scikit-learn  

Install using:  
```bash
pip install -r requirements.txt  
```  

## Usage  
This notebook is designed to run in [Google Colab](https://colab.research.google.com).  
It downloads the MIT-BIH heartbeat data from Kaggle, trains a 1D CNN on the waveform data, and visualizes model performance and learned features.

You will need:  
1. A Google Drive folder containing a valid `kaggle.json` API token.  
2. An internet connection to fetch data from Kaggle.  

To run, open the notebook in Colab and execute all cells sequentially.

## Features  
- 1D Residual CNN for ECG classification  
- Weighted sampling to balance minority classes  
- Focal Loss to improve learning on rare classes  
- Early stopping and learning rate scheduling  
- Confusion matrix, classification report  
- Kernel visualization and saliency mapping for interpretability  

## Configuration  
Main configuration points:  
- Batch size, epochs, and learning rate in the hyperparameter section  
- Focal loss `gamma` value and class weighting  
- Model checkpointing and best model restore  

## Examples  
Example visualizations included:  
- Training and validation loss over time  
- Confusion matrix  
- Learned filter kernels from the first convolutional layer  
- Saliency map highlighting influential waveform regions for a sample beat  

## Future Work and Extension  
- Switch from Kaggle-segmented beats to raw waveform signals for more realistic input  
- Multi-lead ECG support  
- Deploy via TorchScript or ONNX for inference  
- Improve saliency interpretability using Grad-CAM or input optimization  

## References  
No external sources were used. However, LLM queries assisted with architectural design and debugging.  

## Contributing  
No external parties contributed to this project.  

## Licenses  
This project uses data from the MIT-BIH Arrhythmia Database, 
provided by PhysioNet under the Open Data Commons Attribution License v1.0.

Please cite:

Moody GB & Mark RG. The impact of the MIT-BIH Arrhythmia Database. 
IEEE Eng in Med & Biol 20(3):45‑50, 2001.

Goldberger AL, et al. PhysioBank, PhysioToolkit, and PhysioNet. Circulation 101(23):e215–e220, 2000.