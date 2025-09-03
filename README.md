# Driver Drowsiness Detection Using Convolutional Neural Networks

This project addresses the critical public health issue of driver drowsiness, a major contributor to motor vehicle crashes. It utilizes a Convolutional Neural Network (CNN) model to create a non-intrusive, real-time detection system that provides timely warnings to prevent accidents.

---

## Table of Contents
- [Motivation](#motivation)
- [Dataset](#dataset)
- [Methodology](#methodology)
  - [Data Preprocessing](#data-preprocessing)
  - [CNN Architecture](#cnn-architecture)
- [Results](#results)
- [Future Directions](#future-directions)

---

## Motivation

According to the **National Highway Traffic Safety Administration (NHTSA)**, driver drowsiness caused **91,000 accidents** and **50,000 injuries** in 2017.  
In 2019 and 2022, drowsy driving was linked to **697** and **693 fatalities**, respectively.  

A study by the **American Automobile Association's Foundation for Traffic Safety** estimated that drowsy driving accounts for:

- Over **320,000 accidents** annually  
- About **6,400 fatalities** annually  

This suggests that reported figures are likely underestimates.  
The key challenge is to identify drowsiness **quickly and accurately before accidents happen**.

---

## Dataset

The model was developed using the **Driver Drowsiness Dataset (DDD)**, which contains over **41,790 RGB facial images**.

The images are classified into two categories:

- **Drowsy**  
- **Non-Drowsy**

Each image has a resolution of **227x227 pixels**.  
The images were processed using the **Viola-Jones algorithm** to detect and isolate the face region.

---

## Methodology

The project employs a deep learning approach with a **CNN model** specifically designed for facial recognition tasks.

### Data Preprocessing
- **Normalization**: All images were normalized to ensure consistent lighting and color distribution.  
- **Data Augmentation**: Techniques such as rotation, scaling, zooming, and horizontal flipping were applied to create a more diverse dataset.  

### CNN Architecture
The architecture includes:
- Multiple **convolutional layers**  
- **Pooling layers**  
- **Fully connected layers**  
- **Dropout layers** (to prevent overfitting)  

Hyperparameters such as **learning rate**, **batch size**, and **number of epochs** were optimized to improve performance.

---

## Results

- The model achieved an overall accuracy of **~51%**.  
- The classification report shows:
  - More effective at identifying **true negatives (non-drowsy)**  
  - Higher rate of **false negatives (drowsy classified as non-drowsy)** → a **critical safety risk**  
- **F1-score** for both classes: ~0.51 (balance between precision and recall)

---

## Future Directions

Further research will focus on improving the model's performance, especially reducing **false negatives**:

- **More Epochs**: Increase training epochs with **early stopping** and **cross-validation** to avoid overfitting.  
- **Real-time Implementation**: Integrate the model into **in-vehicle monitoring systems**.  
- **Improved Generalization**: Test and refine across:
  - Diverse environmental conditions  
  - Broader demographic variations  
  - Different real-world driving scenarios  

This ensures **universal applicability and reliability**.
