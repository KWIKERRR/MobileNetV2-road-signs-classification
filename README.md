# MobileNetV2 Road Signs Classification

This repository focuses on the classification of road signs into 58 distinct classes using the MobileNetV2 architecture.

## Data

The dataset can be accessed [here](https://www.kaggle.com/datasets/ahemateja19bec1025/traffic-sign-dataset-classification/?select=traffic_Data). The dataset, available in the `trafficData.zip` file, comprises two main folders:

- **DATA:** This folder contains subfolders with images organized by classes. It's worth noting that some classes may have duplicates.
  
- **TEST:** This folder contains images designated for testing the model.

Additionally, the `labels.csv` file provides a mapping of integers to corresponding labels.

## Data Augmentation

Data augmentation is employed to enhance the dataset, incorporating variations through rotation, shear, zoom, width, and height shifts. Notably, flipping is omitted to prevent misinterpretation (e.g., flipping a "don't go left" sign might incorrectly imply a "don't go right" sign).

## Model

The model leverages MobileNetV2 for feature extraction and incorporates dense layers for classification.

## Training

The training process involves two main steps:

1. **Model training:** The MobileNetV2's feature extractor is frozen, and only the classification layers are trained.

2. **Fine-Tuning:** Subsequently, the classification layers are frozen, and the MobileNetV2 is fine-tuned to further refine the model.

## Performance

Post-training, both train and validation accuracy demonstrate a remarkable achievement, reaching up to 99%. This indicates the robustness and effectiveness of the model in accurately classifying road signs.

Feel free to explore and utilize this repository for road sign classification tasks using MobileNetV2. If you encounter any issues or have suggestions for improvement, please don't hesitate to contribute or reach out. Happy coding!
