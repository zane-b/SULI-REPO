
Repo for SULI summer 2021 project. 

      Emulation of the Kessler Microphysics Scheme with Deep Neural Networks
      Zane Bayer (Slippery Rock University, Slippery Rock, PA 17112)
      Valentine Anantharaj and Matthew Norman (Oak Ridge National Laboratory, Oak Ridge, TN 37830)

Numerical weather prediction (NWP) models are now used extensively in weather prediction. NWP models are comprised of many algorithms with varying computational costs. Forecasters and computational scientists are exploring methods to improve the performance of computationally intensive routines within their models. Over the last decade, research has focused on improving computational capacity, physics algorithms, and data assimilation methods, especially for satellite-based sensor data. The rise of deep-learning methods within the natural sciences is significant, but has yet to be thoroughly explored in the context of NWP models. Here, we investigated the applicability of deep neural networks as emulators within these weather models, specifically the Kessler microphysics (KMP) scheme used in NWP models to condense water vapor into rain. We used machine learning models to emulate the KMP scheme. We collected data from the input and output to the Kessler microphysics  subroutine in a NWP model, and trained two sets of machine-learning models for classification and regression. Numerical methods for parameterizations are subject to machine precision in calculations. In some instances, the noise due to machine precision tend to contaminate and confuse machine-learning models. So, our approach is to first train a machine-learning ML model for classifying data samples susceptible to machine precision noise; removing those samples; and then train another machine-learning model to emulate the Kessler microphysics scheme. We also provide linear and decision tree regression baselines for comparison. These baselines allowed us to gauge the potential for improving the performance of the Kessler microphysics  scheme with deep neural networks. Our research showed that machine precision needs to be taken into account when using data from simulation outputs for machine learning.


-Zane Bayer
