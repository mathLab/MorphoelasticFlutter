# MorphoelasticFlutter
A Python implementation of the model proposed in the paper "Nutations in growing plant shoots as a morphoelastic flutter instability" (https://doi.org/10.1098/rsta.2020.0116) 

In this repository you find a standalone Python code that exploits the FEniCS Project Version 2019.1.0 to implement the proposed morphoelastic rod models for growing plant shoots that sense and actively respond to different stimuli (gravitropism, proprioception, and endogenous oscillators), with different tip growth profiles. 

GeneralGrowingShoot.py provide a general way to prescribe tip growth on the subapical growing region of constant length lg, provided that the initial length is larger than lg. Different models for tip growth are provided, and can be selected by commenting and uncommenting the proper expressions for both REGR and REGR_k.

After computing the solution, these codes generate a sequence of images of the 3D rod configuration (see function save_plot) and of its tip projection on the (e1,e3)-plane (see function save_plot2), which are saved in the local subfolders "Movie" and "Movie2", respectively. 
Computed solutions can be saved in the local subfolder "Data" by means of the function save_data(). 
Please, comment out the calls to these functions in order to suppress the undesired output.

Model parameters are all gathered in the "MATERIAL PARAMETERS" section and some specific functions (e.g., to introduce perturbating apical loads) are defined in the "FEM IMPLEMENTATION" section.

If you use this code, we would be grateful if you would cite our publication.
