# A Gravitational Microlensing Detection Algorithm
![alt text](https://avatars0.githubusercontent.com/u/3358238?v=3&s=200)

# Microlensing Detection

This is an open source algorithm that utilizes machine learning to classify a given lightcurve as either a constant source, a cataclysmic variable (CV), an RR Lyrae variable, or a microlensing event. The algorithm uses only the photometric data (magnitude + error) to compute statistical metrics and through the Random Forest algorithm classify the source. 

# Installation

Clone the repository or download to a local system as a ZIP file. 

It's best to work off the same directory in which the package is saved, so that the modules can be called directly, such as: 

from **random_forest_classifier** import **predict_class**

# Required libraries

The code is written entirely in python, and makes use of several familiar packages. They are:
* numpy
* scipy
* astropy
* sklearn

The main module that classifies the lightcurve is the **random_forest_classifier** using the **predict_class** function. It makes use of the module **stats_computation**, which computes the statistical metrics that were used to train the classifier. Note that some of the statistics from **stats_computation** are *not* computed, as they were low-performing and hence omitted to improve the efficiency of the program. 

# Test Script

To make sure that the algorithm is working, please run the following test scripts located in the **test** folder:

* test_script1
* test_script2

Both test scripts should classify the test lightcurve as microlensing. For an additional test, run the **stats_computation_unittest** to ensure that all the statistical metrics are working as intended.

# How to Contribute?

Want to contribute? Bug detections? Comments? Please email us : dg7541@bard.edu, etibachelet@gmail.com, rstreet@lcogt.net
