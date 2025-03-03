# Handwritten Letter Recognition using CNN

This Jupyter Notebook implements a Convolutional Neural Network (CNN) to recognize handwritten letters from a custom dataset.

## Dataset

The dataset consists of handwritten letter images and is organized into three main parts:

-   **letters.zip:** Contains 1650 color images (32x32x3) with 33 different letters. The labels are provided in `letters.txt` and `letters.csv`. Preprocessed image tensors and labels are available in `LetterColorimages.h5`.
-   **letters2.zip:** Contains 5940 color images (32x32x3) with 33 different letters. Labels are in `letters2.txt` and `letters2.csv`. Preprocessed data is in `LetterColorImages2.h5`.
-   **letters3.zip:** Contains 6600 color images (32x32x3) with 33 different letters. Labels are in `letters3.txt` and `letters3.csv`. Preprocessed data is in `LetterColorimages3.h5`.

The letter symbols and corresponding labels are as follows:

-   a => 1, б => 2, B => 3, г => 4, д => 5, е => 6, ё => 7, ж => 8, з => 9, и => 10, й => 11, к => 12, л => 13, м => 14, н => 15, о => 16, п => 17, р => 18, с => 19, т => 20, у => 21, ф => 22, х => 23, ц => 24, ч => 25, ш => 26, щ => 27, ъ => 28, ы => 29, ь => 30, э => 31, ю => 32, я => 33

## Notebook Structure

The notebook is structured as follows:

1.  **Data Loading and Preprocessing:**
    -      Loads the datasets from the provided `.h5` files.
    -      Combines the datasets into a single DataFrame.
    -      Performs data normalization.
    -      Creates DataLoaders for training and validation.

2.  **Model Definition:**
    -      Defines a CNN model using PyTorch.

3.  **Training:**
    -      Trains the CNN model using the training DataLoader.
    -      Calculates training and validation loss and accuracy.
    -      Saves the best model based on validation loss.

4.  **Evaluation:**
    -      Plots the training and validation loss and accuracy curves.
    -      Plots predictions against true labels using the best trained model.

5.  **Prediction Visualization:**
    -   Displays a set of images with predicted and true labels.
    -   Includes a function to map numerical labels back to letter symbols.

## Requirements

-      Python 3.x
-      PyTorch
-      NumPy
-      Matplotlib
-   h5py
-   pandas

## How to Run

1.  Ensure you have all the required libraries installed.
2.  Place the dataset files (`letters.zip`, `letters2.zip`, `letters3.zip`, `LetterColorimages.h5`, `LetterColorImages2.h5`, `LetterColorimages3.h5`, `letters.txt`, `letters2.txt`, `letters.csv`, `letters2.csv`, `letters3.csv`) in the appropriate directory.
3.  Open the Jupyter Notebook and run the cells sequentially.
4.  The trained model (`best_model.pth`) will be saved in the `models` directory.

## Results

The notebook generates plots showing the training and validation loss and accuracy, as well as visualizations of predicted labels against true labels.

## Notes

-   The notebook uses a pre-defined file path to load the best model. Ensure this path is correct or modify it as needed.
-   The normalization parameters used in the notebook are `[0.485, 0.456, 0.406]` and `[0.229, 0.224, 0.225]`. These are standard values for ImageNet, and could be altered.
-   The notebook shows a sample of the prediction results. More detailed analysis could be added.
