# mterms: Multipole terms calculation for the Muon (g-2) storage ring high voltage quadrupole

Authors: Eremey Valetov and Martin Berz  
Organization: Michigan State University  
Email: valetove@msu.edu

## Introduction

This COSY INFINITY program computes multipole terms of the Muon (g-2)
Collaboration quadrupole with adjustable geometry specified by plate distances
and plate voltages specified by the user.

## Requirements

- [COSY INFINITY](https://cosyinfinity.org/)
- MATLAB with the [Schwarz-Christoffel Toolbox](http://www.math.udel.edu/~driscoll/SC/)
  (only needed for generating new conformal map data)

MATLAB must be accessible from the OS command line. This is normally the case
for standard MATLAB installations.

## Quick Start

```
cosy mterms.fox
```

The program will prompt you for:
- Plate distances and voltages (or use the defaults)
- Whether to recalculate conformal map data via MATLAB or use cached data from `mapdata.txt`
- The computation order for multipole terms

Multipole terms are displayed on screen and written to `mterms.txt`.

## Package Contents

| File | Description |
|------|-------------|
| [README.md](README.md) | This file |
| [LICENSE.md](LICENSE.md) | MIT License |
| [mterms.fox](mterms.fox) | COSY INFINITY program |
| [mapdata.txt](mapdata.txt) | Conformal map data for default plate distances and voltages |
| [quad.pdf](quad.pdf) | Plot of the cross-sectional geometry with default distances |

## Geometry Configuration

The polygonal model is stored in the procedure GEOMDATA of mterms.fox.

The x and y coordinates of the polygon are stored in the COSY INFINITY
vectors ZXI and ZYI, respectively. The interior angles of the polygon,
divided by Pi, are stored in the vector ALPHA.

## Calculations

Run the program in COSY INFINITY by entering `cosy mterms.fox` in the command
line. Follow the prompts. Multipole terms will be displayed on screen and
written to the file `mterms.txt`.

If the Schwarz-Christoffel Toolbox is invoked, a plot of the polygonal model
of the cross section with equipotential and field lines is written to the file
`quadplot.pdf`.

## References

- Eremey Valetov. *Field Modeling, Symplectic Tracking, and Spin Decoherence
  for EDM and Muon g-2 Lattices.* Ph.D. thesis, Michigan State University,
  East Lansing, MI, 2017. Fermilab report FERMILAB-THESIS-2017-21.
  [doi:10.2172/1416546](https://doi.org/10.2172/1416546).
- Tobin A. Driscoll. Schwarz-Christoffel Toolbox for MATLAB.
  <http://www.math.udel.edu/~driscoll/SC/>

## License

This project is licensed under the MIT License. See [LICENSE.md](LICENSE.md).
