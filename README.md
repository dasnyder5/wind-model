# wind-model
Sub-task to learn an effective wind model for Nate's wind data for the flowdrone. 

# Data Processing and Training Pipeline: 

Raw data 
   --> Aggregated raw data (files) 
      --> Aggregated raw data (filtered, etc)
         --> Learned prediction model(s) 

## Instructions 1: Raw Data --> Aggregated raw data (files)
This process is done manually; it probably could be automated by a shell script (TODO if deemed important). 
The output of this process is saved under the IRoM Lab Google Drive folder: 

Flowdrone/WindModelData

To get the aggregated raw data (files), download the folders "data_pent/" and "data_hex/"
(note, this will take up approximately 4GB of hard drive space and is NOT necessary if you just need to access the training procedure and/or learned models). 

## Instructions 2: Aggregated raw data (files) --> Aggregated Raw Data (filtered, etc)
This procedure is undertaken in FullDataProcessing.ipynb. Requires the notebook to be in the same directory as data_pent/ and data_hex/ folders.
This procedure outputs aggregated training data in a folder data_agg/, which contains subfolders corresponding to training, testing, and validation data. (TODO: add a script to automatically construct the directories, otherwise might result in a permissions/access issue. Just need to make ~9-12 folders. 

We note again that this procedure can be skipped and the data_agg/. files downloaded directly from the Google Drive in the same folder as above. 

AS BEFORE with data_hex/ and data_pent, the  data_agg/ directory should be in the same directory as the FullDataProcessing.ipynb and NN_Regression*.ipynb notebooks.

## Instructions 3: Aggregated Raw Data (filtered, etc.) --> Learned Prediction Models
This procedure is undertaken in NN_Regression*.ipynb. You will need to make a directory with the following structure (TODO: put this in a shell script):

SavedModels/
--- Angle/
--- Velocity/

This will then construct the necessary models, aggregating best models over 5 random seeds for each setting by default. 
Alternatively (as you can probably guess!), the models can be directly downloaded from the Google Drive folder. The full output is under SavedModels/. in the Google Drive, and the ''best'' models are under best_models/. in the Google Drive. 

