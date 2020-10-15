# MorphoelasticFlutter
A Python implementation of the model proposed in the research paper submitted to Philosophical Transactions of the Royal Society A  

In this repository you find two standalone Python codes that exploit the FEniCS Project Version 2019.1.0 to implement the proposed morphoelastic rod models for 
growing plant shoots that sense and actively respond to different stimuli (gravitropism, proprioception, and endogenous oscillators). 
Different models for tip growth are provided: 
  1. GeneralGrowingShoot.py provide a general way to prescribe tip growth on a subapical growing region of constant length.
  2. GrowingShootEx2.py is an implementation that uses the analytical solution for the growth model given by the Example 2 in the paper.

After computing the solution, these codes generate a sequence of images of the 3D rod configuration (see function save_plot) and of its tip projection on the 
(e1,e3)-plane (see function save_plot2), which are saved in the local subfolders "Movie" and "Movie2", respectively. 
Computed solutions can be saved in the local subfolder "Data" by means of the function save_data(). 
Please, comment out the calls to these functions in order to suppress the undesired output.

Model parameters are all gathered in the "MATERIAL PARAMETERS" section and some specific functions (e.g., to introduce perturbating apical loads) are defined in the 
"FEM IMPLEMENTATION" section.

If you use these codes, we would be grateful if you would cite our publication.
