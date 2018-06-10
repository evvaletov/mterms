
# mterms: Multipole terms calculation for the Muon (g-2) storage ring high voltage quadrupole
Authors: Eremey Valetov and Martin Berz  
Organization: Michigan State University  
Creation date: 03-Feb-2017  
Email: valetove@msu.edu

## 0. Introduction

This COSY INFINITY program computes multipole terms of the Muon (g-2)
Collaboration quadrupole with adjustable geometry specified by plate distances
and plate voltages specified by the user.

For detailed information, including theory and calculation examples, see
the FNAL Report "Main Field of the Muon g-2 Storage Ring High Voltage
Quadrupole" by E. Valetov and M. Berz.

## 1. Package contents

[README.MD](README.MD)	  This file  
[mterms.fox](mterms.fox)	  COSY INFINITY program  
[mapdata.txt](mapdata.txt)	  Conformal map data for default plate distances and voltages  
[quad.pdf](quad.pdf)	  Plot of the cross-sectional geometry with default distances    

## 2. Setup

This program uses COSY INFINITY as the interpreter. It uses MATLAB and
the Schwarz-Christoffel Toolbox for MATLAB by T. Driscoll for calculation of 
polygon prevertices and other parameters.

Please follow the instructions at http://www.math.udel.edu/~driscoll/SC/ to
install the Schwarz-Christoffel Toolbox.

MATLAB must be configured in order for it to run from the OS command line.
This is normally the case for MATLAB installations with no additional action
from the user.

The program was tested to work in Linux and Windows with respective versions
of COSY INFINITY and MATLAB.

## 3. Geometry configuration

The polygonal model is stored in the procedure GEOMDATA of mterms.fox.

The x and y coordinates of the polygon are stored in the COSY INFINITY
vectors ZXI and ZYI, respectively. The interior angles of the polygon,
divided by Pi, are stored in the vector ALPHA.

## 4. Calculations

Run the program in COSY INFINITY, e.g. by entering "cosy mterms.fox" in
the command line. Follow the prompts. Multipole terms will be displayed on
screen and written to file "mterms.txt".

In case the Schwarz-Christoffel Toolbox is invoked, a plot of the polygonal
model of the cross section with equipotential and field lines is written to
the file "quadplot.pdf".

## 5. Copyright Notice
© 2017 Eremey Valetov and Martin Berz