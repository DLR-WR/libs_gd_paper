# Simulation-based calibration-free laser-induced breakdown spectroscopy using gradient optimization (Code Repository)
This repo contains the code used to produce the plots and other results in the paper.
For the simulation code itself, see [LIBSkit](https://github.com/DLR-WR/libskit)


## Quick Start
Create and activate a virtual environment:
```bash
python3 -m venv .venv
source .venv/bin/activate
```

Install the notebook and simulation dependencies:
```bash
pip install -r requirements.txt
```

Then have a look at `gradient_descent_sim_plots.ipynb`.


## Comments
- We put all code in a jupyter notebook for easier iteration
- We use cachi caching in the form of .pkl files (so longer running simulations don't need to be rerun)
- We scaled down max_evals in this repo, plots in the paper were produced with the numbers presented there (e.g. paper sets max_eval for algorithm comparison to 50.000, notebook shows 5000. change if you like)
- There are some additional plots in the notebook that are not in the paper


## Citation
Please cite our paper:

```bibtex
@article{egerland2026,
title = {Simulation-based calibration-free laser-induced breakdown spectroscopy using gradient optimization},
journal = {Spectrochimica Acta Part B: Atomic Spectroscopy},
pages = {107635},
year = {2026},
issn = {0584-8547},
doi = {https://doi.org/10.1016/j.sab.2026.107635},
url = {https://www.sciencedirect.com/science/article/pii/S0584854726001862},
author = {Christoph H. Egerland and Kristin Rammelkamp and Elise Clavé and Ana Lomashvili and Peder Bagge Hansen and Fabian Seel and Susanne Schröder and Heinz-Wilhelm Hübers},
keywords = {LIBS, Optimization, Machine learning},
abstract = {We implement a local gradient-based scheme to fit Laser-Induced Breakdown Spectroscopy (LIBS) spectra to the emission of a uniform, isothermal, stationary plasma in local thermal equilibrium. The gradients of the loss function are obtained by automatic differentiation. We demonstrate the self-consistency and robustness of our fitting scheme through systematic analysis of synthetic spectra and find that, for a wide range of plasma parameters, no additional minimum of the loss function was detected within the investigated parameter domain, enabling reliable recovery of the true parameters.}
}
```

If you use LIBSkit in your research, please cite it:
```bibtex
@software{libskit,
  author  = {Egerland, Christoph H.},
  title   = {LIBSkit: A software tool for the simulation and analysis of
             laser-induced breakdown spectroscopy (LIBS) spectra},
  year    = {2026},
  version = {0.1},
  doi     = {10.5281/zenodo.21788186},
  url     = {https://doi.org/10.5281/zenodo.21788186},
}
```
