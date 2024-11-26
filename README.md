# thesisproject
Related papers and code reproduction
## Project Overview
This repository contains the code and documentation for the reproduction and analysis of two key articles on emulsion modeling:
1. **Kim & Mason (2016)** - Focuses on a free energy model describing the behavior of concentrated monodisperse ionic emulsions, specifically for systems with uniform droplet size.
2. **Jacobs (1999)** - Examines emulsion properties using the Palierne model.

The repository is organized into two main folders, each dedicated to one of the articles.

## Folder Structure

### 1. `Jacobs/`
   - **`Jacobs1999_PalierneBlobs.pdf`**: The original Jacobs (1999) article, which serves as the basis for reproduction and analysis.

### 2. `Kim&Mason/`
  - **`Reference/`**: Contains reference materials, including relevant articles that support the study.
     - **`2014mason.pdf`**: An earlier article by Mason that provides foundational concepts relevant to the 2016 study.
     - **`EEI.pdf`**: Additional reference material related to the free energy model.
   - **`previous code/`**: Stores code versions developed prior to the final reproduction, in Julia and Python languages.
   - **`Kim_Mason_Reproduction.pdf`**: A document summarizing the reproduction process and comparing the results to the original findings.
   - **`py-kimmason-final.ipynb`**: The final code used for reproducing the main results from Kim & Mason (2016).
   - **`py-kimmason-considerT.ipynb`**: Consider temperature T as a variable and calculate the Plateau elastic shear modulus $G'_p$.
   - **`modeltest.ipynb`**: A simplified code to facilitate comparison between experimental data and the results of the EEI model.
   - **`py-kimmason-check.ipynb`**: Supplementary code that includes checks for singularities and other critical points to ensure model accuracy.


<!-- ## Usage
- **Kim & Mason Reproduction**:
  - Use `py-kimmason-final.ipynb` to run the main reproduction of the Kim & Mason model.
  - For additional validation, including singularity checks, refer to `py-kimmason-check.ipynb`.
- **Jacobs Reproduction**:
  - All materials related to the Jacobs article can be found in the `Jacobs/` folder. Future updates may include specific code for reproducing Jacobs' findings. -->

<!-- ## References
- Kim, H.S., Scheffold, F., Mason, T.G. (2016). "Entropic, electrostatic, and interfacial regimes in concentrated disordered ionic emulsions." *Rheologica Acta*, 55, 683-697.
- Jacobs, (1999). *Palierne Blobs in Emulsion Modeling*.

## License
This project is for educational and research purposes. Please cite the original articles if you use or reference this work. -->