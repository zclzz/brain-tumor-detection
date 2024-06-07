# IT1244 Team 3 Project

In this folder, it contains the notebooks for IT1244 Team 3 Porject on Brain Tumor (3.5.2 Brain Tumor Dataset).

## Description

The goal is to conduct binary classification using brain magnetic resonance imaging (MRI) scans to identify whether tumors are present or not.

### Dataset Description

The following lists the different datasets and their description

- Brain_Tumor: Original dataset that is split into Train and Test. Augmentation techniques are applied to the Train set to oversample the images to 122 for each classes.
- cleaned_data: Original dataset is split into Train and Test. Additional Kaggle images added into the Train dataset. Any image duplicates between the original and Kaggle dataset are removed.
- cleaned_data_Wvalidation: Original dataset is split into Train, Valid Test. Kaggle images are only added into the Train dataset. 

Data preprocessing, visualization and data augmentation for oversampling are included in "data_preprocessing.ipynb" and "preprocessing_new_data.ipynb" for the original and new dataset respectively.

## Getting Started
Build a python virtual environment with the corresponding version, select your build-in Python kernel and install any missing dependencies.

### Version History

Python 3.11.2

### Dependencies

Build the dependencies using:
```
pip install -r requirements.txt
```
## Models and Methods

### Traditional ML Models
- KNN, DT, NB and SVM training for original dataset (Brain_Tumor): model_training_original_update.ipynb
- KNN, DT, NB and SVM training for new dataset (cleaned_data): model_training_newdata.ipynb

These notebooks contains the execution of training for all the traditional ML models listed.
The results (accuracy, F1 score and Confusion Matrix) for these baseline models are also included.
<br>
The results for both original and new dataset is exported as csv files in "Results" and "Results_New" folder respectively.

### Neural Network Models
Under the "NN_models" folder,
- datasets: preprocessed, test, valid
- Original CNN (not tuned): Original Simple CNN.ipynb
- Original VGG (not tuned): Original_VGG16.ipynb
- Updated CNN (tuned, optimised): Simple CNN_tuned.ipynb
- Updated VGG (tuned, optimised): VGG16_tuned.ipynb

All the notebooks includes the code to access the dataset, load the dataset and train on it. The trained models are saved as .h5 format which can be used for further testing.

### Tumor Segmentation (WSA)
- wsa_tuned.ipynb

This is a Group 3’s approach to Watershed Segmentation Algorithm. This algorithm not only presents the presence of tumours, it allows medical staff to pin point its exact location, size and shape of the tumour, allowing experts to formulate informed medical procedures. This approach builds and improves on novel approaches by fine tuning parameters and using combinations of different kernels in the preprocess. 

Each step of the algorithm is broken down into the following segments: grayscale, unified sobel, binary thresholding, morphological operations, identifying backgrounds and foreground, optimising unknown regions, final Watershed segmentation. The last segment included the final tuned parameters for the algorithm to generalise a good enough segmentation across the malignant dataset. 

Parameters to be tuned are indicated by comments and segmentation is performed on the raw original data provided to us at the start of the project. 

## Help

All the notebooks are run on Linux/Mac environment. Should any GPU issue arise, push the training to CPU.
<br>
If Window environment is used, please edit the path convention accordingly.

## Authors

IT1244, Team 3:
Zann Lim Jia Min, Lim Chao Zhou, Lei Zhenyu, Darren Wee Cheng Yang"# brain-tumor-detection" 
"# brain-tumor-detection" 
