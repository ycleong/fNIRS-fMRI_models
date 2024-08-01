fNIRS-fMRI Models
================

## Overview of Demo Scripts and Model

This reposistory hosts example scripts and data for training and testing a fNIRS-fMRI predictive model as described in Gao et al. (2024). 

[Demo 1](https://github.com/ycleong/fNIRS-fMRI_models/blob/main/scripts/demo_1.ipynb): Training the model on fNIRS and fMRI participants watching the first half of the first episode of Sherlock

[Demo 2](https://github.com/ycleong/fNIRS-fMRI_models/blob/main/scripts/demo_1.ipynb): Testing the model on fNIRS and fMRI participants watching the second half of the second half of the first episode of Sherlock. Note that here we train and test on the same group of fNIRS participants (watching different stimuli), so accuracy will be inflated. 

## Instructions for Applying the Model

To run this model, start with demo_1, which is the training phase of our
predictive model. In demo_1, the Run 1 fNIRS and fMRI data from all
participants is loaded, and the model is trained on this data. Next, to
test the performance of the trained model, proceed to demo_2, which
contains the testing phase of our predictive model. In demo_2, the Run 2
fNIRS and fMRI data from all participants, along with the model created
in demo_1, are loaded. The model is then tested, and the performance is
calculated and saved into a .mat file.

To run this model on a different dataset, simply replace the fNIRS and
fMRI data in the script. You can modify the data in either the testing
portion, the training portion, or both, depending on your specific
requirements. Please note that we test on the mean fMRI time courses
from a separate group, as these are independent samples. If you have
data from the same subject, this code can be easily adapted to fit the
model to a subject’s fNIRS and test it on the same subject’s fMRI data.
