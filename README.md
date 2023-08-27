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


## Readings of the Data : 
![7b7386d8-9ed9-4dca-91fd-43a607e14164](https://github.com/OmGholap/Cancer-Cell-detection/assets/87529440/59f1e95b-1db8-4197-8c94-2f9695846a2d)

What the above diagram tells us : 
This data is imbalanced for the dx / cell type values as we can see in the next code line also, 

nv       6705
mel      1113
bkl      1099
bcc       514
akiec     327
vasc      142
df        115
Name: dx, dtype: int64

we have a lot how value count for the nv cell type, while the rest of the data is very less. This may give good accuracy 
but in terms of nv and not for other cell types. So data balancing needs to be done.

![92aa461d-3010-44ba-9c37-c1bda5b10721](https://github.com/OmGholap/Cancer-Cell-detection/assets/87529440/952421d3-6e35-4ba1-a3d5-a38b4c3f9275)
![3cb9270a-8119-48b4-b47e-22e349aba9b4](https://github.com/OmGholap/Cancer-Cell-detection/assets/87529440/727306da-dc00-43b1-ab34-35baa25addc4)

the above graph of validation accuracy tells us that the accuracy of the current model is peaking out at 0.77 or 77%. So even if we try to increase the epochs the model might overfit on the data.

What we can try to improve the model : 
changing the layers of the model, the optimiser, and activation functions. etc. 
try using tensorflow data augmentation method instead resample method of sklearn

how the model layer was selected : 
the model configuration was selected using auto keras that suggested we use this architecture of the model, which would result in the best accuracy out of all the combination the autokeras has tried.
