# Multimodal Garbage Classification using EfficientNet and BERT

This project implements a multimodal garbage classification model in PyTorch using both image and text information. The image features are extracted using a pretrained **EfficientNet-B0** CNN, and text features are extracted using a pretrained **BERT-base** model. The text input is automatically generated from the image filename by cleaning and tokenizing it. These features are combined (feature fusion) and passed through fully connected layers to classify each sample into one of four classes: **Black, Blue, Green, and TTR**.

Transfer learning is applied by freezing the BERT layers during initial training and later unfreezing them for fine-tuning. The model is trained using predefined **train, validation, and test sets**, with **CrossEntropyLoss** and the **AdamW optimizer**. Regularization techniques such as **dropout, weight decay, and data augmentation** are used to improve generalization and reduce overfitting.

The training process includes validation monitoring, learning rate scheduling, early stopping, and automatic saving of the best model. The final evaluation includes **test accuracy, confusion matrix, classification report, and visualization of misclassified images**.

The repository contains the complete pipeline for preprocessing, multimodal training, evaluation, and single-image prediction.
