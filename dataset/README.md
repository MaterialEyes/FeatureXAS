# XAS_featurization

`nmc_vasp_xas.json` refers to the computed XAS dataset from VASP. 

`nmc_exp_xas.json` refers to the experimental XAS dataset measured by our collaborators, Chengjun Sun and Inhui Hwang, at Advanced Photon Source at Argonne National Laboratory. 

The detailed data structure for each dataset is shown below:

## nmc_vasp_xas.json

| Property    | Description |
|:---------------- |:------|
| Energy |The X-ray absorption energy in eV |
| Intensity |The XAS intensity in arbitary unit    |
| absorbing_atom_idx |  Site index in structure (e.g., 0)   |
|  structure   | Pymatgen Structure object for VASP-relaxed NMC structures |
|bond_length | Arverage Ni-O bond length in Å|
| composition| NMC composition (e.g., NMC622)|
|oxidation_state|Oxidation state for Ni absorbing atom determined from integrated spin density|


## nmc_exp_xas.json
| Property    | Description |
|:---------------- |:------|
|intensity|Experimental measured XAS intensity interpolated onto energy range of 8330 to 8370eV with 0.4 eV increment |
|cdf|Cumulative distribution function based on intensity |
|peak_feat|Peak feature based on intensity  |
|cwt|Continuous wavelet transform based on intensity |
|voltage|Experimentally measured voltage in volt |
|composition|NMC composition (e.g., NMC622) |
