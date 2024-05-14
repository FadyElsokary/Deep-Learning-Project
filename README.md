

**Project Overview:**

Our team embarked on a project to develop a Convolutional Neural Network (CNN) model for actor image classification. The objective was to accurately identify actors Karim AbdelAziz, Hend Sabry, and Hany Ramzy from images. The project involved rigorous data preparation, model architecture design, training, and evaluation to achieve optimal classification accuracy.



**Model Architecture Visualization:**

The CNN model comprised multiple convolutional layers grouped into ConvBlocks, each followed by pooling layers for feature extraction and spatial reduction. The configuration included:

- ConvBlock 1:
  - Number of Filters: 5
  - Filter Size: (3, 3, 3)
  - Pooling Size: (2, 2)
- ConvBlock 2:
  - Number of Filters: 5
  - Filter Size: (3, 3, 3)
  - Pooling Size: (2, 2)
- ConvBlock 3:
  - Number of Filters: 5
  - Filter Size: (3, 3, 3)
  - Pooling Size: (2, 2)
- Flattening Layer: Converts output to a flattened form

**Layer Dimensions and In/Out Data:**

- ConvBlock 1:
  - Input: Batch size x 512 x 512 x 3
  - Output after Convolution: Batch size x 510 x 510 x 5
  - Output after Pooling: Batch size x 255 x 255 x 5
- ConvBlock 2:
  - Input: Batch size x 255 x 255 x 5
  - Output after Convolution: Batch size x 253 x 253 x 5
  - Output after Pooling: Batch size x 126 x 126 x 5
- ConvBlock 3:
  - Input: Batch size x 126 x 126 x 5
  - Output after Convolution: Batch size x 124 x 124 x 5
  - Output after Pooling: Batch size x 62 x 62 x 5
- Flattening Layer:
  - Input: Batch size x 62 x 62 x 5
  - Output: Batch size x 19220

**Model Hyperparameters and Training Details:**

The model utilized filter sizes of (3, 3, 3) and pooling sizes of (2, 2) across all ConvBlocks. ReLU activation replaced Sigmoid for improved accuracy. K-means clustering aided in feature extraction and prediction, achieving 44.53% accuracy.

**Training and Evaluation:**

Training involved mapping labels to numerical IDs, shuffling data, fixing format inconsistencies, and converting images to RGB. The model trained for 55 epochs with a batch size of 32, utilizing Adam optimizer (lr=0.001) and categorical cross-entropy loss. The trained model achieved 90.73% accuracy during testing on unseen data.

**Conclusion:**

Our CNN model successfully classified images of actors with 90.73% accuracy. The methodology encompassed robust data preparation, optimized model architecture, and effective training strategies. Future enhancements may focus on hyperparameter fine-tuning, alternative architectures, or data augmentation techniques for enhanced robustness and generalization.
