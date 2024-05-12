# Rock-Paper-Scissors Image Classification Project

## Overview

The Rock-Paper-Scissors (RPS) game in this project serves as a useful and exemplary image classification application. The instructions below will guide you through the project's code and the datasets involved.

## Dataset Creation

1. **CreateDatasetMulti.py**
   - Run command: `python CreateDatasetMulti.py <path_to_dataset_directory>`
   - Converts raw images of dimension 400x400 to a matrix and saves it as a .pkl file. It also shuffles the points.
   - Example: `Datasetpkl_sample` consists of sample .pkl files after running CreateDatasetMulit.py.

2. **CombineDatasets.py**
   - Run command: `python CombineDatasets.py <folder_path>`
   - Combines multiple .pkl dataset files into one large `combine_dataset.pkl` file which the models train on.

3. **gather_images.py**
   - Run command: `python gather_images.py class_name no_of_images`
   - Automatically collects images of the specified number, using the webcam to rapidly capture pictures and saves the dataset images in a folder of the given class_name.

4. **Training Dataset**: `combined_dataset_testing.py`
5. **Testing Dataset**: `combined_dataset_training.py`

## Models

1. **Trained_Model**
   - Directory consists of all the trained models as .pkl files, which can be loaded using Python joblib and used for analysis or live prediction.

2. **Model_Evaluation**
   - Directory consists of .ipynb files for all the model analyses, with a separate folder for each. It also includes a Cross-validation evaluation .ipynb file between all the models.

3. **PresRecall4.py**
   - Run command: `python PresRecall4.py dataset_path.pkl model_path.pkl`
   - Calculates the precision-recall for a given model and dataset. It is used only for testing purposes.

## Live Prediction

1. **LivePred.py**
   - Run command: `python LivePred3.py <model_path.pkl>`
   - Performs predictions on live data. The webcam is used to get a stream of images, and the predictions are sequentially printed in the terminal.

2. **live_feed_lndmrk.py**
   - Run command: `python live_feed_lndmrk.py`
   - Used for the representation of Mediapipe’s hand landmarking feature.

