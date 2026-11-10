# Code for _Controlling energy delivery with bistable nanostructures_

The source code in this repository allows to perform the numerical calculations and generate the essential data presented in Figures 4, 6, and 7 of the manuscript [_Controlling energy delivery with bistable nanostructures_](https://doi.org/10.1103/llzj-hmxz).

<img width="982" height="810" alt="key_image" src="https://github.com/user-attachments/assets/b01075a7-a2b3-4308-a92b-2059ce1b27e5" />

``A two-state source nanostructure (blue) uses an energy-delivery mechanism akin to ATP hydrolysis to power a nanomachine (black) through a two-stage coupled relaxation process. © Andreas Ehrmann''


## Getting started
To run the scripts, simply run the ``slurm_array.sh`` script on your cluster using a Python environment to run an ensemble of long Brownian Dynamics simulations. This will import all relevant packages and run long Brownian Dynamics simulations for an ensemble of Machine-only systems using the code ``individual_simulation_state.py`` or simulations of an ensemble of coupled systems of Machine & Source at a fixed binding energy $\epsilon$ using the code ``coupled_simulation_state.py`` and save relevant data.
The data contains information about the Machine actions and the measures of merit of the energy-delivery mechanism: performance, power, and efficiency as well as the number of Machine actions and the number of Source recharging events.
For varying binding energies $\epsilon$, change the corresponding parameter in the main python script ``coupled_simulation_state.py`` and save the data in separate folders for the analysis.

After that, running the ``Analysis.ipynb`` notebook will help analyzing the data, extracting the relevant measures of merit, and producing the corresponding figures.

Comments 
1. All parts of the code scripts and the analysis notebook that require user input are marked with TODOs.
2. This work is based on the Python libraries [_JAX_](https://github.com/jax-ml/jax) and [_JAX MD_](https://github.com/jax-md/jax-md).

List of required Python libraries and packages that need to be installed in a pip environment:
- jax, jax_md, jaxopt
- scipy, matplotlib, os, sys, pickle, xarray, typing
- common_utils ([_git.ista.ac.at/goodrichgroup/common_utils_](https://git.ista.ac.at/goodrichgroup/common_utils))

## Citation

Andreas Ehrmann and Carl P. Goodrich, _Controlling energy delivery with bistable nanostructures_, [Physical Review X (2026)](https://doi.org/10.1103/llzj-hmxz).

```
@article{ehrm26,
  title = {Controlling energy delivery with bistable nanostructures},
  author = {Ehrmann, Andreas and Goodrich, Carl P.},
  year = {2026},
  journal = {Physical Review X},
  doi = {10.1103/llzj-hmxz),
}
```
