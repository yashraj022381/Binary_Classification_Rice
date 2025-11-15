# Binary_Classification_Rice


This project implements a binary classification model using a neural network to distinguish between two types of rice grains: Cammeo and Osmancik. 

The classification is based on seven physical and geometric features extracted from the rice grains.

  1. ⚙️ Setup and Environment:
     This project is designed to be run entirely in a Google Colaboratory environment, which provides the necessary                   dependencies and computational resources.

     (i) Prerequisites
        The following Python packages are required and are installed in the first code cell of the provided Colab notebook,           Binary_Classfication_Rice.ipynb:

        google-ml-edu==0.1.2

        keras~=3.8.0

        matplotlib~=3.10.0

        numpy~=2.0.0

        pandas~=2.2.0

        tensorflow~=2.18.0

     (ii) Installation Steps (Google Colab)
       - Open the Notebook: Upload and open the Binary_Classfication_Rice.ipynb file in Google Colab.

       - Install Dependencies: Run the first code cell (usually labeled In [1]) which contains the !pip install command to             install all necessary libraries.

     Python

     !pip install google-ml-edu==0.1.2 \
         keras~=3.8.0 \
         matplotlib~=3.10.0 \
         numpy~=2.0.0 \
         pandas~=2.2.0 \
         tensorflow~=2.18.0

     - Run Imports: Run the subsequent cell to import the Python libraries and set display options for pandas.

     - Execute Remaining Cells: Step through the rest of the notebook cells sequentially to load the data, preprocess the            features, train the neural network model, and evaluate its performance.
    


   2. 💾 Dataset:
      - The model uses the Rice_Cammeo_Osmancik dataset, which is a publicly available dataset hosted by Google.

         - Source URL: https://download.mlcc.google.com/mledu-datasets/Rice_Cammeo_Osmancik.csv

         - Total Records: 3810 rice grain samples

         - Target Variable: Class (which is one of 'Cammeo' or 'Osmancik')

         - Features: The dataset includes 7 quantitative features:

            - Area

            - Perimeter

            - Major_Axis_Length

            - Minor_Axis_Length

            - Eccentricity

            - Convex_Area
          

  3. 📊 Model and Results:-
     
      (i) Data Preprocessing:
        - Label Encoding: The categorical Class column is converted into a binary numerical format for the classification                task.
        - Feature Standardization: All numerical features are standardized to have a mean of 0 and a standard deviation of 1.
        - Data Split: The data is split into training, validation, and test sets.

      (ii) Model Architecture:
         - The model is a Feed-Forward Neural Network (DNN) built with Keras and typically consists of a sequence of Dense               layers.
         - The model is compiled using an Adam optimizer and trained for 60 epochs.
             - Training Metrics: The notebook tracks several metrics, including accuracy, AUC (Area Under the Curve), loss,                  precision, and recall.

     (iii) Summary of Final Performance:
         - The notebook's final evaluation metrics compare the training and validation performance:

       Metric	       Training Set Value	       Validation Set Value
      Accuracy	          0.9252	                   0.8950
        AUC	              0.9793	                   0.9722
       Loss	              0.1844	                   0.2155
      Precision	          0.8858	                   0.8449
       Recall	            0.9481	                   0.9349

        -  These results suggest the model performs well at the binary classification task, with high AUC and accuracy scores             on both training and validation data.
