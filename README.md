# Pathology Detection in Crop Plants  

## Overview  
This project investigates automated classification of diseases in apple leaves using advanced machine learning and deep learning techniques. Leveraging a high-quality image dataset, we combine traditional machine learning models and convolutional neural networks (CNNs) to develop scalable methods for plant disease detection. The proposed approaches support technology-driven solutions for sustainable agriculture.  

---

## Team Members  
- **Domenico Azzarito**  
- **Guillermo Bajo Laborda**  
- **Laura Alejandra Moreno**  
- **Arian Gharehmohammadzadehghashghaei**  
- **Michele Pezza**  

---

## Dataset  
The dataset is sourced from the Kaggle competition: [Plant Pathology 2020 - FGVC7](https://www.kaggle.com/competitions/plant-pathology-2020-fgvc7). It contains 1,821 labeled images of apple leaves categorized into four classes:  

- **Healthy**: No visible symptoms of disease.  
- **Rust**: Fungal infections with rust-like symptoms.  
- **Scab**: Fungal lesions causing scab-like patterns.  
- **Multiple Diseases**: Symptoms of more than one disease present.  

---

## Methodology  

### Exploratory Data Analysis (EDA)  
- **Class Distribution:** Visualized using pie charts and histograms, highlighting the imbalance in the "Multiple Diseases" class.  
- **Color Analysis:** Computed RGB histograms and channel statistics to identify class-specific patterns in leaf images.  

### Preprocessing  
- **Edge Detection:** Applied Canny filtering to isolate leaf regions and remove background noise.  
- **Feature Engineering:** Extracted RGB histograms and Gray-Level Co-occurrence Matrix (GLCM) features for machine learning models.  
- **Data Augmentation:** Addressed class imbalance through synthetic oversampling and geometric transformations.  

### Machine Learning Models  
1. **Softmax Regression:** Baseline multiclass prediction model.  
2. **Random Forest:** Ensemble learning method to improve accuracy.  

### Deep Learning Models  
1. **ResNet-50**  
   - Fine-tuned residual connections to capture complex hierarchical features.  
   - Addressed gradient issues through skip connections.  
2. **VGG-16**  
   - Optimized sequential layers for extracting fine-grained patterns.  
   - Balanced depth and simplicity for efficient classification.  

---

## Results  

### Performance Comparison  

| Model                | Accuracy  |
|----------------------|-----------|
| Softmax Regression   | 77.0%     |
| Random Forest        | 81.1%     |
| ResNet-50            | 83.52%    |
| VGG-16               | **86.81%** |

### Per-Class Performance  

| Class                | ResNet-50 Recall | VGG-16 Recall |
|----------------------|------------------|---------------|
| Healthy              | 81.0%            | 87.9%         |
| Multiple Diseases    | 10.0%            | 30.0%         |
| Rust                 | 92.2%            | 90.6%         |
| Scab                 | 90.0%            | 92.0%         |

---

### Key Observations  
- **VGG-16:** Achieved the highest accuracy of **86.81%**, handling fine-grained features effectively.  
- **ResNet-50:** Performed well (**83.52%**) but struggled with rare categories due to fewer samples and complexity.  
- **Random Forest:** Outperformed Softmax Regression, emphasizing the need for non-linear decision boundaries.  
- **Class Imbalance:** The "Multiple Diseases" class remained a challenge, highlighting the need for oversampling and augmentation techniques.  

---

## Future Work  
- **Model Improvements:** Fine-tune CNN architectures with learning rate schedules and dropout enhancements.  
- **Advanced Networks:** Evaluate modern architectures like EfficientNet and Vision Transformers for improved scalability and accuracy.  
- **Preprocessing Enhancements:** Integrate leaf segmentation and de-noising algorithms to enhance image clarity.  
- **Imbalance Handling:** Expand augmentation methods, including generative approaches, to enrich minority classes.  
- **Mobile Deployment:** Develop lightweight models for mobile and IoT platforms, enabling real-time disease detection in agricultural fields.  

---

## Conclusion  
This study demonstrated the potential of combining traditional machine learning techniques with modern CNN architectures for plant disease detection. While CNNs like **VGG-16** and **ResNet-50** achieved high accuracy, challenges remain in handling underrepresented classes.  

### Key Findings:  
- CNNs outperformed traditional models, achieving accuracies of **86.81% (VGG-16)** and **83.52% (ResNet-50)**.  
- Random Forest achieved **81.1%**, highlighting the effectiveness of ensemble methods.  
- Softmax Regression served as a baseline with **77.0%** accuracy.  
- Class imbalance, especially in the "Multiple Diseases" category, limits model performance, emphasizing the need for targeted augmentation and oversampling.  

---

## Roles  
- **Arian Gharehmohammadzadehghashghaei:** Exploratory Data Analysis and Model Evaluation.  
- **Laura Alejandra Moreno and Guillermo Bajo Laborda:** Machine Learning Models (Softmax, Random Forest).  
- **Domenico Azzarito and Michele Pezza:** Deep Learning Models (CNNs - ResNet-50, VGG-16).  

---

## References  
- Kaggle Dataset: [Plant Pathology 2020 - FGVC7](https://www.kaggle.com/competitions/plant-pathology-2020-fgvc7)  
- Mohanty, Sharada P., David P. Hughes, and Marcel Salathé. "Using deep learning for image-based plant disease detection." Frontiers in plant science 7 (2016): 1419.  
