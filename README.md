<h1 align="center">
ANALYSIS AND MODELING OF LOCOMOTION - PROJECT 3 - README
</h1>

## Team members

- Albrecht Alice
- Juanico Alice
- Testa Laura

## Data story

You can find the entire data story of this project on the complete report, called `AML_Project3_datastory.pdf` in the respository.

## Structure of the repository

To allow the compiling of the given code it's necessary to have the same respository organization then indicate below.

The repository is composed of 4 folders:
- `data`: composed of 2 subfolders:
    - `Healthy_data`: which contains the raw data of the healthy patient for 3 conditions.
    - `SCI Human`: which contains the raw data of the spinal cord injured patient for 3 conditions.
- `processed_data`: where the process files of the 6 datasets will be stored.
- `results`: where the PCA results will be stored.
- `scripts`: which contains the following coding files:
    - `gait_cycle_extraction.m`: function that preprocess kinematics and extract the gait cycles.
    - `gait_cycle_stickplots.m`: function that allow a great visualization of one gait cycle per condition.
    - `EMG_preprocessing.m`: function that preprocess EMG data to obtain linear envelopes.
    - `kinematic_features_extraction.m`: function taht extract all the features from kinematics data preprocessed.
    - `EMG_features_extraction.m`: function that extract every all the features from EMG data preprocessed.
    - `process_file.m`: function that perform the complete processing of one file by calling all predefined functions.
    - `main.m`: 

## Setup

- To perform the entire analysis you just have to run the `main.m` file. 
- We let you the possibility to show the processing plots by modfing in the `main.m` file at line 2:
    `get_plots = 'False'` into `get_plots = 'True'`
    The value is False by default to make the compiling of the code quicker. 

### Methods
To go through the complete analysis we performed multiple steps:
- Gait cycle extraction: Kinematics data are used to extract the gait cycles.
- EMG pre-processing: the EMG data is prepared for the feature extraction.
- EMG, kinematics features extraction: a list of specific features are extracted from the experimental data for each gait cycle.
- Principal Component Analysis (PCA): PCA is performed on the extracted features to compare injured and healthy locomotion.
- Visualization: results are visualized to better compare the locomotions.
- Statistical tests: statistical tests are performed to assess the critical parameters for a healthy locomotion