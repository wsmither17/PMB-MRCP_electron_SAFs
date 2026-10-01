# Electron SAFs for the ICRP MRCPs

Electron specific aborbed fractions (SAFs) for the ICRP family of mesh-type reference
computational phantoms (MRCPs), accompanying:

> Smither W W, Choi C, Shin B, Jokisch D W,
> Mate-Kole E M, Dewji S A, Bolch W E.
> *Electron Specific Absorbed Fractions for the ICRP Family of Mesh-Type 
> Reference Computational Phantoms.* Physics in Medicine & Biology (2026).

Data are provided for **twelve phantoms**: both sexes (`M`, `F`) at six ages
(**newborn, 1-year-old, 5-years-old, 10-years-old, 15-years-old, adult**). Throughout the filenames,
`MRCP_<AgeSex>` identifies a unique phantom — e.g. `MRCP_00F` is the newborn female phantom.



Acronyms (the **Short Name** column of the region-mapping tables, e.g. `Brain`,
`GB-wall`, `R-marrow`) are the same codes used in the `Source` and `Target` columns of the
SAF files. Definitions can be found in Tables 1 (`Source regions`) and 2 (`Target regions`).

## Specific absorbed fractions — `MRCP_<AgeSex>_Electron_SAF.xlsx` (12 files)

Specific absorbed fractions are expressed in **kg⁻¹**, with one file
per phantom.

```
Target,Source,<0.000>,<0.001>, … ,<10.000>
```

Each data row is one target-source pair (86 sources x 62 targets = 5,332 pairs). The remaining columns give the SAF at each monoenergetic source electron energy (in **MeV**). Electron PHITS simulations were run on a logarithmic grid from 10 keV to 10 MeV (25 datapoints). A limiting value at 0 MeV was computed following Eqns. 8-10 along with interpolated values at 1 and 5 keV (3 datapoints) for a total of 28 datapoints per target-source pair (Columns C:AD). A zero value at an energy greater than 0 MeV is one in which the calculated collisional + radiative SAF was found to be zero - i.e. a PHITS collisional tally + photon SAF of zero.

## Data source files — `SAF_origin.xlsx`
**`SAF_origin.xlsx`** provides the provenance of a specific target-source pair applicable to all 12 phantoms, whether directly calculated in this study, taken from **Shin *et al* (2025)**, or from **ICRP Publication 155 (2023)**.

## Change Log
**`1 October 2026:`** Updated README.md, uploaded finalized data, added SAF_origin.xlsx.


