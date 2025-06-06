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

DFT_heatmap
============
This folder contains a script for plotting several heatmaps, such as magnetic states, magnetic moment, and formation energy. The heatmaps are plotted based on the B^i sites of the first layer (MnBi2Te4). Since there are four different B^i sites (Bi, Sb, Sn, Pb), the dataset is converted into four pivot tables and then plotted separately.
The heatmaps related to the substrate effect analysis are also plotted. Only the case of B^i = Bi has been shown. The associated Jupyter notebook: plots_hetero_ACS_AMI_Review.ipynb.

Preprocessing
=============
In this folder, the feature elimination process for predicting Mu, magnetic states, and lattice mismatch has been performed. For the prediction of formation energy and the band gap, the first descriptor set is used without any feature elimination process. For predicting other properties, the second and third sets of descriptors have been used with several steps of feature elimination, including calculating the Pearson correlation coefficient to remove duplicate descriptors, plotting each descriptor against the target property, and so on. The final sets of descriptors are then fed into the ML models. The associated Jupyter notebook: Features_Elimination_for_Mu_AND_Mismatch.ipynb

Results_Ef
==========
Performance of feed-forward neural network (FFNN), random forest, and XGBoost regression models in predicting the formation energy of heterostructures.
The associated Jupyter notebooks: Formation_Energy_FFNN.ipynb, Formation_Energy_RF_Regression.ipynb, Formation_Energy_XGB_Regression.ipynb.

Results_Eg
==========
Performance of FFNN, random forest, and XGBoost regression models in predicting the band gap of heterostructures.
The associated Jupyter notebooks: Bandgap_FFNN.ipynb, Bandgap_RF_Regression.ipynb, Bandgap_XGB_Regression.ipynb.

Results_Mu
==========
Performance of random forest and XGBoost regression models in predicting the magnetic moment of heterostructures. 
The associated Jupyter notebooks: Magnetic_Moment_XGBoost.ipynb, Magnetic_Moment_FFNN.ipynb.

Results_Mag_States
==================
Performance of extra trees, support vector machine, and XGBoost classification models in predicting the magnetic states of heterostructures.
The associated Jupyter notebooks: Mag_States_Classification_ET.ipynb, Mag_States_Classification_SVM.ipynb, Mag_States_Classification_XGBoost.ipynb

Results_Mismatch
================
Performance of FFNN, random forest, and XGBoost regression models in predicting the lattice mismatch of heterostructures. 
The associated Jupyter notebooks: Lattice_Mismatch_FFNN.ipynb, Lattice_Mismatch_RF.ipynb, Lattice_Mismatch_XGBoost.ipynb.


