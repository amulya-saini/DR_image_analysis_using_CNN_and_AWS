# Diabetic Retinopathy Detection and Classification Using Deep Learning (CNN)

## Kaggle Eye Disease Detection Project

## Overview
This project aims to detect Diabetic Retinopathy using a dataset obtained from a 2015 Kaggle competition. The dataset consists of retinal images labeled with different disease severity levels(0-4). The project utilizes AWS services for data preprocessing, model training, and evaluation.

Severity Labels:

0 - No DR
1 - Mild
2 - Moderate
3 - Severe
4 - Proliferative DR

## Preprocessing
- The dataset is retrieved from a 2015 Kaggle competition and stored in an S3 bucket.
- Images are downloaded from S3 to an EC2 instance using Boto3.
- Image preprocessing steps include resizing, blur detection, data augmentation, and organization into labeled folders.

## Model Training
- Transfer learning is employed using the fastai library with a DenseNet201 architecture.
- Learning rate analysis is performed to determine optimal learning rates and weight decay parameters.
- The model is trained using the 1cycle policy for improved convergence and generalization.
- Validation data is moved from the training set to evaluate model performance.
- Confusion matrix analysis is conducted to assess classification accuracy.

## Grad-CAM Visualization
- Gradient-weighted Class Activation Mapping (Grad-CAM) is used to visualize important image regions influencing model predictions.
- Heatmaps are generated to highlight areas of interest for both correct and incorrect predictions.
- Visualization aids in understanding model decision-making and identifying areas for improvement.

## Project Structure
- `image_preprocessing.ipynb`: Jupyter Notebook containing data preprocessing code.
- `learning_rate_and_model_architecture.ipynb`: Notebook for model training and evaluation.
- `training_and_roc.ipynb`: Notebook for Grad-CAM visualization.

## Usage
1. Clone the repository.
2. Install required dependencies using `pip install package'.
3. Run Jupyter notebooks sequentially for preprocessing, model training, and visualization.
4. Modify parameters and experiment with different architectures as needed.

## Results
- The trained model achieves a validation accuracy of 86.85%.
- Grad-CAM visualization provides insights into model predictions and areas of focus.

## Future Work
- Explore additional preprocessing techniques for improved model performance.
- Experiment with different architectures and hyperparameters to enhance accuracy.
- Investigate ensemble methods and model distillation for further optimization.

## Acknowledgments
- Kaggle for providing the dataset and hosting the competition.
- AWS for cloud computing resources used in this project.
- Fastai community for valuable deep learning insights and tools.


