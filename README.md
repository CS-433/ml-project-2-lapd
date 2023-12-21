# LAPD ML project 
## Dataset 
There are two datasets. The first one can be found here on the github page in the model C folder. The second data will be provided in a different way as it contains images and is therefore too heavy for the github. We recommend running this code on google colab to avoid having to change the code too much for the import of the data. When running each file make sure all the data is at the same level and that the path to the data is correct (google drive preferably). 
## Files 
Cloud detector : This folder contains a notebook with different functions defined to detect clouds
Model A_b : This folder contains the code used to make model A_b as well as the saved model (.pt) and the saved predictions (.pkl) 
Model B : This folder contains the code used to make model B as well as the saved model (.pt) and the saved predictions (.pkl)
Model C : This folder contains the code used to make model C as well as the saved model (.pt) and the saved predictions (.pkl). This folder also contains some extra files as preprocessing had to be done for this model. The raw data, preprocessed data, means and standard deviations, and median/Q1/Q3 can also be found in this folder. A helper.py and the preprocessing notebook corresponding to this model can also be found here.
Model D : This folder contains the code used to make model D as well as the saved model (.pt) and the saved predictions (.pkl)
Model A1 : This folder contains the code used to make model A1. For reproducibility purposes you can run the code which loads the saved model (model1_meteo_after_LSTM2.pt). Images included in this folder represent the prediction made with this model on the validation sets.
Original_Code_Keras.ipynb : This is the original code given to us by the lab as a basis. 
Saved model and comparison: This folder contains pickle files with the predictions done by each model. It also contains a notebook (result.ipynb) in which the different predictions are plotted together for analysis/comparison purposes.
Schematic: This folder contains powerpoint files with schematics of our network architectures.
Visualisation: This folder contains the code (notebook) used to make the visualisation and the saved images.



[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/fEFF99tU)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-718a45dd9cf7e7f842a935f5ebbe5719a5e09af4491e668f4dbf3b35d5cca122.svg)](https://classroom.github.com/online_ide?assignment_repo_id=12971902&assignment_repo_type=AssignmentRepo)
