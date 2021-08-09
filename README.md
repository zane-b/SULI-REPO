# Introduction

      Emulation of the Kessler Microphysics Scheme with Deep Neural Networks
      Zane Bayer (Slippery Rock University, Slippery Rock, PA 17112)
      Valentine Anantharaj and Matthew Norman (Oak Ridge National Laboratory, Oak Ridge, TN 37830)

Numerical weather prediction (NWP) models are now used extensively in weather prediction. NWP models are comprised of many algorithms with varying computational costs. Forecasters and computational scientists are exploring methods to improve the performance of computationally intensive routines within their models. Over the last decade, research has focused on improving computational capacity, physics algorithms, and data assimilation methods, especially for satellite-based sensor data. The rise of deep-learning methods within the natural sciences is significant, but has yet to be thoroughly explored in the context of NWP models. Here, we investigated the applicability of deep neural networks as emulators within these weather models, specifically the Kessler microphysics (KMP) scheme used in NWP models to condense water vapor into rain. We used machine learning models to emulate the KMP scheme. We collected data from the input and output to the Kessler microphysics  subroutine in a NWP model, and trained two sets of machine-learning models for classification and regression. Numerical methods for parameterizations are subject to machine precision in calculations. In some instances, the noise due to machine precision tend to contaminate and confuse machine-learning models. So, our approach is to first train a machine-learning ML model for classifying data samples susceptible to machine precision noise; removing those samples; and then train another machine-learning model to emulate the Kessler microphysics scheme. We also provide linear and decision tree regression baselines for comparison. These baselines allowed us to gauge the potential for improving the performance of the Kessler microphysics  scheme with deep neural networks. Our research showed that machine precision needs to be taken into account when using data from simulation outputs for machine learning.


For an in-depth description of the KMP scheme, see https://doi.org/10.1016/j.cageo.2012.10.006. The dataset was gathered from an ORNL numeric weather model and consists of 24 million input/output samples. The notebook includes the methods used to calulate statisitics of the dataset and to emulate the KMP scheme using sklearn models. We used python 3.8 to develop the emulators.

# MicroPhysics Notebook
The microPhysNB.ipynb notebook includes the methods used to calulate statisitics of the dataset and to emulate the KMP scheme using sklearn models. We used python 3.8 to develop the emulators. The models were developed using the sklearn library.

# SULI Report
The technical report is provided for further reading on the methods and results of our study.


## ACKNOWLEDGEMENT
This code was written by Zane Bayer and Valentine Anantharaj. We would like to thank Matthew Norman for supplying the dataset and assistance with the project. This research used resources of the Oak Ridge Leadership Computing Facility, which is a DOE Office of Science User Facility, and the resources of the Compute and Data Environment for Science (CADES) at the Oak Ridge National Laboratory, both supported by the Office of Science of the U.S. Department of Energy under Contract DE-AC05-00OR22725.
