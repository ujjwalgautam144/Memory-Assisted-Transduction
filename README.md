# Memory-Assisted-Transduction

Repository for experimental data and analysis assets related to memory-assisted transduction measurements.

## Contents

- `Experimental_Plots.ipynb`  
	Main analysis notebook for loading data and generating figures.

- `Absorption Data/`  
	Absorption-spectrum inputs and calibration settings.
	- `4g-1e-Spectrum-1000MHz_to_3620MHz.bin`
	- `Cal_file.settings`

- `Full_Sequence_Data/`  
	Time-sequence measurement runs organized by date/experiment name.
	Each run folder typically contains:
	- `Cal_file.settings`
	- many compressed traces in `.gzip` format

	Example run folders:
	- `01Apr25_MW_frequency_2/`
	- `10May25_MW_ON_OFF_Run4/`
	- `10May25_Temporal_Modes/`
	- `18July25_Interference_MW1_MW2_Phases_7/`

- `Plots/`  
	Exported/derived figure outputs (currently includes `4g_1e_optical_depth_fit.pdf`).

## Data Naming Conventions

Common trace filename pattern:

`Frequency_<frequency_in_kHz>kHz_f_<shot_index>.gzip`

Example:

`Frequency_2622800kHz_f_0.gzip`

where:
- `<frequency_in_kHz>` is the microwave (or scan) frequency label
- `<shot_index>` is the repeated acquisition index for that setting

## Calibration Settings

Several folders include `Cal_file.settings`, typically storing acquisition scaling/offset parameters (for example `x_div`, `y_div`, `voltage_offset`).

## Usage

1. Open `Experimental_Plots.ipynb` in Jupyter (VS Code or JupyterLab).
2. Point notebook paths to the desired run folder under `Full_Sequence_Data/`.
3. Execute cells to load traces, process signals, and generate figures.

## Notes

- This repository is primarily data + analysis notebook assets.
- If additional acquisition/source code exists outside this workspace, link it here for reproducibility.
