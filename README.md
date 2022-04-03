# Contents
 * Introduction
 * System and Environment Requirements
 * Dataset

## Introduction
A case study to devise 3 feature engineering strategies to predict whether a patient will develop Central Neuropathic Pain. The 3 strategies developed are then compared to determine which one is better w.r.t. performance of prediction.

## System and Environment Requirements
To run this project, your system needs the following software - 
1. Jupyter Notebook (via Anaconda Navigator)/Google Collab
2. Python 3.7 or above (Packages - numpy, matplotlib.pyplot and sklearn (scikit-learn))

## Dataset
The data is preprocessed brain EEG data from SCI patients recorded while resting with eyes closed (EC) and eyes opened (EO).
 * 48 electrodes recording electrical activity of the brain at 250 Hz
 * 2 classes: subject will / will not develop neuropathic pain within 6 months
 * 18 subjects: 10 developed pain and 8 didn’t develop pain
 * The data has already undergone some preprocessing
   * Signal denoising and normalization
   * Temporal segmentation
   * Frequency band power estimation
   * Normalization with respect to total band power
   * Features include normalized alpha, beta, theta band power while eyes closed, eyes opened, and taking the ratio of eo/ec.
 * The data is provided in a single table ('data.csv') consisting of
   * 180 rows (18 subjects x 10 repetitions), each containing
   * 432 columns (9 features x 48 electrodes) 
   * rows are in subject major order, i.e. rows 0-9 are all samples from subject 0, rows 10-19 all samples from subject 1, etc.
   * columns are in feature_type major order, i.e. columns 0-47 are alpha band power, eyes closed, electrodes 0-48
   * feature identifiers for all columns are stored in ___feature_names.csv___
   * ___labels.csv___ defines the corresponding class (0 or 1) to each row in data.csv
