fNIRS-fMRI Models
================

## Overview of Demo Scripts and Model

This reposistory hosts example scripts and data for training and testing a fNIRS-fMRI predictive model. A trained version of the model is available: https://github.com/ycleong/fNIRS-fMRI_models/blob/main/models/sherlock_run1model.pickle. We note that the scripts and model in this repository differ slightly from those described in Gao et al. (2024), where the model was trained and tested using a leave-one-participant-out approach, resulting in 29 separate models. In this repository, the model is trained on data from all participants, providing a single model for general use.

[Demo 1](https://github.com/ycleong/fNIRS-fMRI_models/blob/main/scripts/demo_1.ipynb): Training the model on fNIRS and fMRI participants watching the first half of the first episode of Sherlock

[Demo 2](https://github.com/ycleong/fNIRS-fMRI_models/blob/main/scripts/demo_1.ipynb): Testing the model on fNIRS and fMRI participants watching the second half of the second half of the first episode of Sherlock. 

To run this model on a different dataset, simply replace the fNIRS and
fMRI data in the scripts. You can modify the data in either the testing
portion, the training portion, or both, depending on your specific
requirements. Please note that we test on the mean fMRI time courses
from a separate group, as these are independent samples. If you have
data from the same subject, this code can be adapted to fit the
model to a subject’s fNIRS and test it on the same subject’s fMRI data.
