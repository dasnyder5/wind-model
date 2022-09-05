# wind-model
Sub-task to learn an effective wind model for Nate's wind data for the flowdrone. 

# Overview // Pipeline: 

Raw data 
   --> Aggregated raw data (files) 
      --> Aggregated raw data (filtered, etc)
         --> Learned prediction model(s) 

# Instructions 1: Raw Data --> Aggregated raw data
This process is done manually; probably could be automated by a shell script (TODO if deemed important). 
The output of this process is saved under the Google Drive folder 

irom-lab\Projects\Flowdrone\WindModelData

To get the aggregated raw data (files), download the folders "\data_pent" and "data_hex\"
(note, this will take up approximately 4GB of hard drive space). 

# Instructions 2: Aggregated raw data (files) --> Aggregated Raw Data (filtered, etc)
This procedure is undertaken in FullDataProcessing.ipynb. Requires the notebook to be in the same directory as data\_pent and data\_hex folders. 
