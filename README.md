# Thesis Project
## Project Overview
This repository contains reproducible notebooks, references and supporting scripts for the study of (mainly emulsion) rheology. It reproduces landmark models (Jacobs 1999 - Palierne model; Kim & Mason 2016 - EEI model) for simulating droplet stacking for a given volume fraction. All notebooks are written in Python, rely only on open source libraries, and can be run interactively in Jupyter Lab. 

**For confidentiality reasons, the raw experimental data used in some notebooks is not included in this repository.**  


The repository is organized into three main folders.

## Folder Structure

### 1. `Jacobs/`
   - **`Jacobs1999_PalierneBlobs.pdf`**: The original Jacobs (1999) article, which serves as the basis for reproduction and analysis.
   - **`py-Jacobs-1.ipynb`**: Implements the Palierne emulsion viscoelastic model presented in Jacobs (1999).  
     * Re-creates all core equations (monodisperse and continuous droplet distributions) and the explicit relaxation times $λ_F, λ_b$.  
     * Reproduces the paper’s $G',G''$ curves (Fig. 1–2) by droplet radius, interfacial tension, and moduli.  
     * Provides interactive sliders (ipywidgets) for sensitivity analysis of the interfacial tension $\alpha$, saving publication-ready plots and CSV summaries.
     * A example for the monomodal v.s. bimodal case, show the difference for the shear modulus under different situations.

   - **`DataFittingforFrequencySweepModels.ipynb`**: Fits raw frequency-sweep rheology data with a suite of classical viscoelastic models.  
     * Includes Palieren, Generalized Maxwell, Kelvin-Voigt and combined implementations.  
     * Uses lmfit for global non-linear least squares, ranks models via AIC/BIC and residual norms, and exports best-fit parameters, diagnostic plots, and residual tables to `results/{sample}/{model}/`.  
     * Generates corner plots for parameter correlations and an overlay of experimental points with fitted curves for quick visual inspection.

   - **`mayob.ipynb`**: Foucs on the mayob sample, using a combination of maxwell and kelvin-voigt models to match rate all data, high frequency data, and low frequency data, respectively.
  


### 2. `Kim&Mason/`
   - **`2014mason.pdf`**: An earlier article by Mason that provides foundational concepts relevant to the 2016 study.
   - **`EEI.pdf`**: Reference material related to the free energy model.
   - **`py-kimmason-final.ipynb`**:  Implements the electrostatic–entropic–interfacial (EEI) model proposed by Kim & Mason (2016) for emulsions.  
      * Builds the full free-energy landscape *F = F<sub>int</sub> + F<sub>ent</sub> + F<sub>elec</sub>* and determines the equilibrium deformed-droplet fraction φ<sub>d</sub> via numerical minimisation.  
      * Calculates the plateau elastic shear modulus *G<sub>p</sub>* and osmotic Pressure $\pi$, visualises its dependence on droplet volume fraction, strain rate, droplet radius, ionic strength, and surface potential.  
   - **`py-kimmason-considerT.ipynb`**: Consider temperature T as a variable and calculate the Plateau elastic shear modulus $G'_p$.
   - **`py-kimmason-modeltest_final.ipynb`**: Applies the EEI model to experimental frequency-sweep data from five mayonnaise-like emulsions.  
      * Loads sample metadata (T, *a*, ionic strength, surface tension, ζ-potential) and performs global as well as sample-specific non-linear least-squares fits to extract the optimal entropic coefficient α and electrostatic coefficient ξ.  
      * Ranks fits with error, overlays model curves on the experimental *G<sub>p</sub>*–φ data (log‐scale), and summarises best-fit parameters.  
      * Generates corner plots for parameter covariance and a master curve comparing all samples, facilitating quick visual validation of model performance.


### 3. `volume fraction/`
   - **`RSA.ipynb`**: Quick 2-D random-sequential-adsorption (RSA) simulator for droplets.  
      * Packs polydisperse circles in a square box until no more can fit.  
      * Lets you tweak droplet size distribution (log-normal), box size *L*, and RNG seed.  
      * Outputs final area fraction, list of (x, y, r) coordinates, and a PNG of the packing.

## License
This project is for educational and research purposes. Please cite the original articles if you use or reference this work.