# Code_YeastCoop

## Article

This code was used to solve a numerical model of sucrose and glucose diffusion in a 1D yeast cooperator/cheater system. 
Additional information can be found here : 

Le Bec et al., Optogenetic spatial patterning of cooperation in yeast population, BioRXiv, 2023. 

Experimental and numerical datasets are available here : https://zenodo.org/deposit/7908455

## Details and how to run the script.

To model the growth of yeast in sucrose, we use Michaelis–Menten kinetics for enzymatic reactions (invertase hydrolysis), high and low affinity glucose transporter and Monod equation for the yeast growth rate.

To solve the PDE we use a python package called scikit-fdiff (https://scikit-fdiff.readthedocs.io).
We chose the Crack-Nicholson scheme to compute the diffusion of molecule across a discretized space and used reflective boundaries. We use a simulation hook to compute non-linear terms and prevent negatives values.

The discretization of the time and space dimension has been carefully chosen to respect the following relation:
∆t << ∆x²/ DM
Values were typically ∆t = 2 sec and ∆x = 1e − 4 m

To run a simulation in the Jupyter script, several packages need to be installed. You can also directly download an anaconda environment containing all required packages with the following link:
https://anaconda.org/matthias.lebec/cellmodeling



