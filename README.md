# Code_YeastCoop

To model the growth of yeast in sucrose, we use Michaelis–Menten kinetics for enzymatic reactions (invertase hydrolysis), high and low affinity glucose transporter and Monod equation for the yeast growth rate.

To solve the PDE we use a python package called scikit-fdiff (https://scikit-fdiff.readthedocs.io).
We chose the Crack-Nicholson scheme to compute the diffusion of molecule across a discretized space and used reflective boundaries. We use a simulation hook to compute non-linear terms and prevent negatives values.

The discretization of the time and space dimension has been carefully chosen to respect the following relation:
∆t << ∆x²/ DM
Values were typically ∆t = 2 sec and ∆x = 1e − 4 m

To run a simulation in the Jupyter script, several packages need to be installed. You can also directly download an anaconda environment containing all required packages with the following link:
https://anaconda.org/matthias.lebec/cellmodeling
