# Paint vs. Pixel: Distinguishing Real vs A.I Generated Artwork. (MIE1517 Group Project 2023)
This github repo contains all the code and data necessary to understand and reproduce the results of our group project focusing on classifying real vs AI generated art works using a neural network classifier, implemented in pytorch.

This project was done for the graduate level course  *[Introduction to Deep Learning (MIE1517)](https://www.mie.utoronto.ca/programs/graduate/course-descriptions/#MIE1517H)* at the University of Toronto in Fall 2023.
The main contributors to this project are
- [Jensen Zhao](https://www.linkedin.com/in/jensen-zhao)
- [Riley Moher](https://linktr.ee/rileymomo)
- [Parnian Azimzadeh](https://www.linkedin.com/in/parnian-azimzadeh)

##  Overview
This repo contains datasets, jupyter notebooks, and other project-related files used to perform the main art classification task. It is organized as follows:

 - Data folder - Each dataset consists of 256x256 .jpg images
	 - cropped_paintings_256.zip - Contains the set of pre-processed image files from the WikiArt dataset
	 - cropped_diffusiondb_256.zip - Contains the set of pre-processed image files from the Diffusiondb Dataset
    	 - ai_data_new.zip - Contains AI-generated images sourced from Chat-GPT4 for the purposes of classification on brand new data
         - human_data_new.zip - Contains human-made images sourced from artmatch.ca for the purposes of classification on brand new data
 - Notebooks
	 - wiki_art_processing.ipynb - loading and pre-processing for human-artist data
	 - diffusiondb_processing.ipynb - loading and pre-processing for ai-generated data
	 - MIE1517_Group10_Final_Report.ipynb - contains the main work of the project, loading both datasets, creating and training the model, and performing the classification task
	 - new_data_testing.ipynb - demonstrates the model's capabilities on completely unseen data from new data sources, including Chat-GPT4/Dall E 3 generated images, and artworks from artmatch.ca
 - Media Folder
	 - MIE1517 Project Presentation Video - Team10 Final.mp4 - The final edited video presentation for the project
	 - MIE1517 Team 10 Project Presentation.pdf - the exported accompanying slides from the video presentation

## Get Started
The main component of the project is contained in the MIE1517_Group10_Final_Report.ipynb notebook - this loads in the two pre-processed datasets, defines the CNN classifier, trains the model, and saves checkpoints during training. Since both pre-processed datasets are provided in the data folder, the model can be used or modified directly from this notebook without the need to load the original datasets. 

To recreate the full end-to-end project, you will also need to run the data processing notebooks, wiki_art_processing.ipynb and diffusiondb_processing.ipynb, to create your own copies of the datasets (here you can also modify the crop function to experiment with different sizes, or different filtering techniques for the selection of the data). 
