# Pathology Detection in Crop Plants

## Overview

This project aims to classify diseases in apple leaves using advanced machine learning techniques. By leveraging a high-quality image dataset and applying both traditional machine learning methods and deep learning models, the study explores effective approaches to detect and classify plant diseases, contributing to technology-driven agricultural practices.

## Team Members
- **Domenico Azzarito**
- **Guillermo Bajo Laborda**
- **Laura Alejandra Moreno**
- **Arian Gharehmohammadzadehghashghaei**
- **Michele Pezza**

## Dataset
The dataset is sourced from the Kaggle competition: [Plant Pathology 2020 - FGVC7](https://www.kaggle.com/competitions/plant-pathology-2020-fgvc7/). It contains 1,821 labeled images of apple leaves categorized into four classes:
- **Healthy**: Leaves without disease symptoms.
- **Rust**: Leaves affected by rust-like fungal pathogens.
- **Scab**: Leaves with scab lesions caused by fungal infections.
- **Multiple Diseases**: Leaves showing symptoms of more than one disease.

## Methodology

### Exploratory Data Analysis (EDA)
- Visualized class distribution using pie charts and bar graphs.
- Analyzed mean RGB channel intensities for each class to uncover patterns.

### Preprocessing
- Applied edge detection (Canny) to crop leaf regions and eliminate background noise.
- Extracted RGB histograms as features for traditional machine learning models.
- Performed data augmentation to address class imbalance.

### Machine Learning Models
1. **Softmax Regression**: Used as a baseline for multiclass classification.
2. **Random Forest**: Enhanced accuracy through ensemble learning techniques.

### Deep Learning Models
1. **ResNet-50**:
   - Pretrained on ImageNet and fine-tuned for this dataset.
   - Used skip connections to ensure stable training and robust performance.
2. **VGG-16**:
   - Fine-tuned a simple yet effective architecture.
   - Captured detailed hierarchical features for disease classification.

## Results
- **Softmax Regression**: Accuracy of ~44%.
- **Random Forest**: Accuracy of ~71%.
- **ResNet-50**: Achieved the highest accuracy of 86.81%.
- **VGG-16**: Closely followed with an accuracy of 86.26%.

Both CNN models showed strong performance but struggled with the underrepresented "Multiple Diseases" class. Augmentation and class balancing are areas for improvement.

## Future Work
- Fine-tune CNN models by optimizing learning rates and dropout layers.
- Develop and evaluate a custom CNN tailored to the dataset.
- Explore advanced architectures like Vision Transformers or EfficientNet.
- Enhance data preprocessing with leaf segmentation and noise reduction.


