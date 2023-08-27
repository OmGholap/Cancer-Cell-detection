# Cancer-Cell-detection
Objective: Develop a robust and accurate skin cancer lesion classification system that identifies various types of skin cancer lesions from images. The primary goal is to create a model that offers reliable diagnostics, while also addressing class imbalance challenges for optimal performance across all lesion types.

Project Highlights:

Data Collection and Exploration:

Utilized the HAM10000 dataset containing seven classes of skin cancer lesions.
Analyzed data distribution, identifying significant class imbalance.
Data Preprocessing and Augmentation:

Cleaned and balanced the dataset using resampling to ensure equal representation of each lesion type.
Resized images to a consistent size of 32x32 pixels.
Normalized pixel values to the range of 0-1.
Model Architecture:

Constructed a Convolutional Neural Network (CNN) model for image classification.
Designed a model architecture based on AutoKeras suggestions, optimizing for accuracy.
Incorporated convolutional layers, pooling layers, dropout layers, and fully connected layers.
Utilized ReLU activation functions for feature extraction.
Model Training:

Split the dataset into training and testing sets.
Trained the model using categorical cross-entropy loss and Adam optimizer.
Applied data augmentation techniques to enhance model generalization.
Evaluation and Analysis:

Evaluated model performance using accuracy, loss, and confusion matrix.
Identified areas of potential improvement based on accuracy, precision, recall, and F1-score for each class.
Results and Insights:

Achieved a peak validation accuracy of approximately 77%.
Confusion matrix analysis highlighted specific areas where the model excelled and where improvements were needed.
Recognized the challenge of class imbalance and its impact on model performance.
