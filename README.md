# thesisproject
Related papers and code reproduction
## Project Overview
This repository contains the code and documentation for the reproduction and analysis of two key articles on emulsion modeling:
1. **Kim & Mason (2016)** - Focuses on a free energy minimization model describing the behavior of concentrated monodisperse ionic emulsions, specifically for systems with uniform droplet size.
2. **Jacobs (1999)** - Examines emulsion properties using the Palierne model.

The repository is organized into three main folders, each dedicated to one of the articles.

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
      * Calculates the plateau elastic shear modulus *G<sub>p</sub>* and visualises its dependence on droplet volume fraction φ, strain rate γ̇, droplet radius *a*, ionic strength, and surface potential.  
      * Provides interactive `ipywidgets` sliders plus 3-D surface/contour plots for rapid sensitivity analysis, and exports publication-ready figures (`figures/*.png`) as well as CSV tables of *G<sub>p</sub>* vs φ.

   - **`py-kimmason-considerT.ipynb`**: Consider temperature T as a variable and calculate the Plateau elastic shear modulus $G'_p$.
   - **`py-kimmason-modeltest_final.ipynb`**: A simplified code to facilitate comparison between experimental data and the results of the EEI model.


### 3. `volume fraction/`
   - **`RSA.ipynb`**:

## License
This project is for educational and research purposes. Please cite the original articles if you use or reference this work. -->