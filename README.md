# Chest_X_ray_Classification
Classification_Pneumonie_Covid_Normal

This repository contains codes for challenge hosted by Trustii. 
The dataset is not public and was just provided for the challenge. It was constituted of radiographies of normal chest, pneumonic chest and covid chest in png format.

The first model present a classification 2 by 2 (3 classifiers) and then a final classifier retake each layers outputs of each classifier and reinjected them into the next layer.

The second modele consist to train U-shape autoencoders on each class and them save each resulted image from them for all radiographies(part_1). Then all images obtained for one radiography are injected in CNN to classified them.
The saving of all outputs of the first part allow better computation time for the second part because it avoid recalculation of the auoencoders outputs for each training steps of the classifier.
We noted that the val_accuracy is better than the training accuracy mainly because images are augmented for the training step contrary to the validation step.

The third model is an adaptation from a model described in the paper: Shastri, S., Kansal, I., Kumar, S. et al. CheXImageNet: a novel architecture for accurate classification of Covid-19 with chest x-ray digital images using deep convolutional neural networks. Health Technol. 12, 193-204 (2022). https://doi.org/10.1007/s12553-021-00630-x.
The different outputs of the three autoencoder are injected in the CNN to achieve good accuracy.
This project was interesting to handle medical images and I learned to always follow what operations is performed on images by visualizing them at each steps of the preprocessing.
