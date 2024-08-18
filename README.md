# VegNet - A CNN-Based Image Classification System for Vegetables and Market Scenes

**Project Overview:**

VegNet is a deep learning project aimed at creating a powerful multiclass image classification system capable of identifying and categorizing various types of vegetables, including onions, potatoes, and tomatoes, as well as distinguishing market scenes. The project tackles the challenge of accurately classifying agricultural produce images, which is critical for automating processes in the fresh produce supply chain industry.

**Dataset:**

The dataset comprises thousands of images scraped from the web, organized into four primary classes: onions, potatoes, tomatoes, and Indian market scenes. Additionally, the model is designed to identify and label images that do not belong to any of these categories as noise, enhancing its robustness in real-world applications.

**Model Architecture:**

The project experimented with several Convolutional Neural Network (CNN) models to identify the optimal architecture for the classification task:

1. **Custom Sequential CNN Model:** A model built from scratch with convolutional layers, followed by max-pooling, global average pooling, dense layers, and a softmax output layer for multiclass classification.

2. **Pre-trained VGG16 Model:** A transfer learning approach using the VGG16 architecture pre-trained on ImageNet, with its convolutional base utilized for feature extraction and custom fully connected layers added for specific classification needs.

3. **Pre-trained ResNet50 Model:** Another transfer learning model leveraging the ResNet50 architecture, also pre-trained on ImageNet, with additional custom layers designed to adapt the model for classifying vegetable images and market scenes.

4. **Pre-trained InceptionV3 Model:** A transfer learning model using the InceptionV3 architecture, where the convolutional layers were retained and custom layers were integrated to fine-tune the model for the specific classification tasks in this project.

**Training and Optimization:**

- **Data Preprocessing:** Images were resized to 128x128 pixels and normalized to ensure consistency across the dataset. Data augmentation techniques were employed to artificially expand the dataset and improve the model’s generalization capabilities.

- **Hyperparameter Tuning:** The Adam optimizer was used with categorical crossentropy as the loss function. Early stopping and model checkpointing were implemented to prevent overfitting and to save the best-performing model based on validation accuracy.

- **Performance:** The models were trained and evaluated using a split dataset (training, validation, and test sets), achieving a consistent improvement in accuracy across multiple epochs.

**Conclusion:**

VegNet successfully demonstrates the application of CNNs in solving complex image classification problems in the agricultural domain. By experimenting with multiple architectures, including custom-built and pre-trained models, the project highlights the technical implementation and addresses real-world challenges by ensuring the model is scalable, accurate, and capable of handling diverse inputs.
