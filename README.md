fNIRS-fMRI Models
================

## Overview of Demo Scripts and Model

This demo script is available as a tool to train and apply our model on
other datasets. Within this script, we have created a model that is
trained on fNIRS and fMRI data from the first half of a movie stimulus.
Following this training, the model is then tested on the fNIRS and fMRI
data from the second portion of the movie stimulus. This model slightly
differs from the model utilized in our analysis as we incorporated a
leave-one-subject-out (LOO) in our original model.

For the demo model, we removed the LOO component of the training phase
in order to get a single model from all of the run 1 data. For the
testing phase, the model is still tested on the held-out run (run 2) so
that the model was not tested on data that it had been priorly trained
on. Maintaining the same subjects in training and testing improves the
model performance which provides a higher model performance within the
demo than what is reported in the paper.

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

## Data Format

For the specifics regarding data format, we have created this model to
take in the fNIRS and fMRI data as a 3D matrix that contains number of
subjects by timepoint by number of ROIs. For the fMRI data used in this
model, there should not be any NaNs present within matrices. These NaNs
can be adjusted for by imputing using the mean, which was a component of
our initial analysis. On the other hand, the fNIRS data can have NaNs
present in the matrices. The modeling scripts will impute by taking the
mean of all other subjects.
