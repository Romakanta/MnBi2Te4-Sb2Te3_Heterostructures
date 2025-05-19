# MnBi2Te4-Sb2Te3_Heterostructures
Data analytics and machine learning models on MnBi2Te4/Sb2Te3-type heterostructures. 
Various types of ML models have been employed, such as random forest, xgboost, support vector machine, FFNN....
A short description of the files/folders is given below.

MBT_CONTCARs
============
This folder contains 240 candidate MnBi2Te4-type monolayer structures from the MBT monolayer project. The results of this project have been published in the Journal of Materials Chemistry C. See https://pubs.rsc.org/en/content/articlelanding/2023/tc/d3tc00001j/unauth for details. In this project, for constructing the MnBi2Te4/Sb2Te3-type heterostructures, I used 240 candidate MBT-type monolayers and 12 Sb2Te3-type structures to find the lattice mismatch between the two stacking layers.

Descriptors
============
In this folder, I have done two things. First, I calculated the lattice mismatch between the (above-mentioned) MnBi2Te4-type monolayers using the 'MBT_CONTCARs' folder and the Sb2Te3-type monolayers using the script 'Find_Lattice_Mismatch.ipynb'. The two stacking layers are considered to construct the heterostructures such that the magnitude of lattice mismatch between the layers doesn't exceed 3%. 891 candidate heterostructures satisfy this criterion.
Next, I constructed the descriptors for candidate structures using the Mendeleev Python package. The descriptors are constructed by applying some mathematical operations on the atomic properties of the constituent elements in the candidate structures. Three sets of descriptors are constructed. The first set is for predicting the formation energy and the band gap, the second set is for predicting the magnetic properties (preferred magnetic configurations and the total magnetic moment), and the last set is for predicting the lattice mismatch between the two stacking layers.

