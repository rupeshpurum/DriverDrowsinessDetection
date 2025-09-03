Driver Drowsiness Detection Using Convolutional Neural Networks
This project addresses the critical public health issue of driver drowsiness, a major contributor to motor vehicle crashes. It utilizes a Convolutional Neural Network (CNN) model to create a non-intrusive, real-time detection system that provides timely warnings to prevent accidents.

Motivation
According to the National Highway Traffic Safety Administration (NHTSA), driver drowsiness caused 91,000 accidents and 50,000 injuries in 2017. In 2019 and 2022, drowsy driving was linked to 697 and 693 fatalities, respectively. A study by the American Automobile Association's foundation for traffic safety estimated that drowsy driving accounts for over 320,000 accidents and 6,400 fatalities annually, suggesting that reported figures are likely underestimates. The key challenge is to identify drowsiness quickly and accurately before accidents happen.

Dataset
The model was developed using the Driver Drowsiness Dataset (DDD), which contains over 41,790 RGB facial images.

The images are classified into two categories:

Drowsy

Non-Drowsy

Each image has a resolution of 227x227 pixels. The images were processed using the Viola-Jones algorithm to detect and isolate the face region.

Methodology
The project employs a deep learning approach with a CNN model specifically designed for facial recognition tasks.

The data was preprocessed to enhance model robustness:

Normalization: All images were normalized to ensure consistent lighting and color distribution.

Data Augmentation: Techniques such as rotation, scaling, zooming, and horizontal flipping were applied to create a more diverse dataset.

The CNN architecture includes multiple convolutional layers, pooling layers, fully connected layers, and dropout layers to prevent overfitting. Hyperparameters like learning rate, batch size, and number of epochs were optimized to improve performance.

Results
The model achieved an overall accuracy of approximately 51%. The classification report indicates that the model is more effective at identifying true negative (non-drowsy) instances but has a higher rate of false negatives, which represents a critical safety risk. The F1-score for both classes is approximately 0.51, reflecting a balance between precision and recall.

Future Directions
Further research will focus on improving the model's performance, particularly by addressing the challenges posed by false negatives. This can be achieved through:

More Epochs: Increasing the number of training epochs to allow the model to learn more complex patterns, while using techniques like early stopping and cross-validation to prevent overfitting.

Real-time Implementation: Integrating the model into real-time monitoring systems within vehicles.

Improved Generalization: Testing and refining the model's performance across diverse environmental settings and a broader range of demographic variations to ensure universal applicability and reliability.
