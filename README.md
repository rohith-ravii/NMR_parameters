# Peptide Molecular Dynamics Analysis

This repository contains Jupyter notebooks for analyzing molecular dynamics (MD) simulations of peptides, with a focus on membrane environments. The primary analyses include calculating ²H quadrupolar splitting and chemical shift anisotropy (CSA).

## Jupyter Notebooks

### `hydrogen_qudrapolar_splitting.ipynb`

This notebook calculates the tilt angle and ²H quadrupolar splitting for peptide segments within a membrane.

**Functionality:**
- Loads molecular structure (`.gro`) and trajectory (`.xtc`) files.
- Aligns the trajectory to a reference structure.
- Calculates the tilt angle of peptide segments relative to the membrane normal.
- Computes the ²H quadrupolar splitting based on the peptide's orientation.
- Generates plots of the distributions for tilt angle and quadrupolar splitting.
- Saves the results to a CSV file.

### `chemical_shift.ipynb`

This notebook is designed to calculate chemical shift anisotropy (CSA) and orient a peptide structure based on experimental data.

**Functionality:**
- Calculates the principal axes of the chemical shift tensor.
- Determines the θ and φ angles which describe the orientation of the peptide relative to the membrane.
- Computes the σ_zz component of the chemical shift tensor.
- Includes a script to orient a peptide PDB structure based on experimental quadrupolar splitting and CSA data.
- Generates plots for the distributions of σ_zz, θ, and φ.
- Saves the results to CSV files.

## Dependencies

The notebooks rely on the following Python libraries:

- [MDAnalysis](https://www.mdanalysis.org/)
- [NumPy](https://numpy.org/)
- [Pandas](https://pandas.pydata.org/)
- [Matplotlib](https://matplotlib.org/)
- [SciPy](https://scipy.org/)

These can be installed via pip or conda. For example:
```bash
pip install mdanalysis numpy pandas matplotlib scipy
```

## Usage

To use these notebooks for your own data, you will need to modify the file paths within the notebook cells.

1.  **Set `data_dir`**: In both notebooks, update the `data_dir` variable to the directory containing your simulation files.
2.  **Specify file names**: Update `gro_name` and `xtc_names` to match your structure and trajectory files.
3.  **Adjust parameters**: Modify parameters such as `residue_number` and `copies` to fit your specific system.
4.  **Run the notebook**: Execute the cells in the notebook to perform the analysis.
