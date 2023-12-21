# LAPD ML project - Predictic GHI from meteo data and webcam images

Welcome to the LAPD GHI prediction repository! As societies worldwide strive to embrace sustainable energy, Switzerland stands out with a remarkable increase in photovoltaic power generation. In 2022, photovoltaic installations alone contributed a substantial 3858 GWh, a significant leap from 299 GWh in 2012 [source: Federal Office of Energy Statistics, 2023](https://www.swissolar.ch/03_angebot/news-und-medien/statistik-sonnenenergie/statistique_energie_solaire_2022_rapport_fr_final.pdf). This surge in solar energy production underscores the growing impact on the Swiss power grid.

In response to the dynamic nature of solar power, energy companies face the challenge of predicting and optimizing grid performance. Traditional methods rely on meteorological companies that employ satellite imagery and complex algorithms to forecast Global Horizontal Irradiance (GHI), a key metric tied to solar panel performance. However, existing predictions often lack spatial resolution for small areas and may not be highly accurate within specific timeframes [source: Solcast](https://solcast.com/).

This GitHub repository introduces a machine learning solution to address these challenges. Our goal is to develop an algorithm capable of generating precise local predictions of GHI two hours into the future. Leveraging meteorological data, such as wind, current GHI, date, etc., and webcam images from two EPFL campus cameras, we tried to enhance the accuracy of short-term GHI predictions highly locally. This project have been proposed by the Laboratory of Applied Photonics Devices (LAPD) [source: LAPD](https://www.epfl.ch/labs/lapd/) and takes part of the ML4Science initiative proposed by the Machine Learning course (CS-433) at EPFL.

Feel free to explore the code, datasets, and documentation to gain insights into our machine learning approach for accurate GHI predictions.

## Github organization

<img width="899" alt="Screenshot 2023-12-21 at 14 24 46" src="https://github.com/CS-433/ml-project-2-lapd/assets/62161504/9979262a-32a0-41da-bef7-45dc589e226d">

### models

Each model have it own folder, containing the python notebook of the model, the saved best model (.pt) and the saved result on the validation sets (.pkl)

- **Model A_a**:                      
This folder contains the code used to make model A1. For reproducibility purposes you can run the code which loads the saved model (model1_meteo_after_LSTM2.pt). Images included in this folder represent the prediction made with this model on the validation sets.
- **Model A_b**:                     
This folder contains the code used to make model A_b as well as the saved model (.pt) and the saved predictions (.pkl)     
- **Model B**:                       
This folder contains the code used to make model B as well as the saved model (.pt) and the saved predictions (.pkl)   
- **Model C**:                      
This folder contains the code used to make model C as well as the saved model (.pt) and the saved predictions (.pkl). This folder also contains some extra files as preprocessing had to be done for this model. The raw data, preprocessed data, means and standard deviations, and median/Q1/Q3 can also be found in this folder. A helper.py and the preprocessing notebook corresponding to this model can also be found here.   
- **Model D**:                       
This folder contains the code used to make model D as well as the saved model (.pt) and the saved predictions (.pkl)  

- **Saved model and comparison** :   
This folder contains pickle files with the predictions done by each model. It also contains a notebook (result.ipynb) in which the different predictions are plotted together for analysis/comparison purposes.
**Schematic**:                     
This folder contains powerpoint files with schematics of our network architectures.  

### visualisation 

- **Visualisation**:                
This folder contains the code (notebook) used to make the visualisation and the saved images. 


### custom features

- **Cloud detector**:               
This folder contains a notebook with different functions defined to detect clouds   

### original code

- **Original_Code_Keras.ipynb** :    
This is the original code given to us by the lab as a basis.

## Dataset 

Due to it size (especially for images), we will not provide the full dataset directely on the github. 
There are two datasets. 

- meteo only dataset : can be found here on the github page in the model C folder.
- meteo + images dataset : provided in a different way as it contains images and is therefore too heavy for the github.  The dataset is available at this [link](https://drive.google.com/drive/folders/1ujAD2dnhsZ6ZLCeC5Ofk3leqiW_bv8UH?usp=sharing)

## Running the code 

We recommend running this code on google colab to avoid having to change the code too much for the import of the data. When running each file make sure all the data is at the same level and that the path to the data is correct (google drive preferably). This means that to run e.g. model B, all the dataset files must be in a folder along with model_B.pt to make the importation work. The path that you should initialize is 'drive/MyDrive/\<your-path-in-your-google-drive\>' and can be changed at the beginning of each notebook.

To run a file :
1. open google collab and import the targeted notebook
2. open your drive and import the dataset on a "data" folder. Upload the .pt and the .pkl corresponding to the notebook/model in the same folder (more generally, upload the content of the git folder in the drive folder)
3. open the notebook and update the path to the data
4. make sure you meet all the requierement in the requierement.txt
5. if you don't want to retrain the model, run all the cells before the training, run the model loading below the training and run the validation to obtain the result.


[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/fEFF99tU)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-718a45dd9cf7e7f842a935f5ebbe5719a5e09af4491e668f4dbf3b35d5cca122.svg)](https://classroom.github.com/online_ide?assignment_repo_id=12971902&assignment_repo_type=AssignmentRepo)
