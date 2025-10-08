# foamGyroid
Example of simulation setup in OpenFOAM to mesh a single periodic cell of a TPMS, then simulate it using periodic hydraulic and thermal boundary conditions.

## Software requirements
The case was developed and tested in [OpenFOAM v2212](https://www.openfoam.com/download/release-history#v2212).

## Usage
In the folder ```constant/triSurface``` a geometry must be inserted, in .stl format, with dimension 10x10x10 (possbly larger to avoid problems when cut in blockMesh).
Within ```system/controlDict``` and ```system/controlDictScalar``` two new function objects are used, that you might find in  

Run the ./Allrun file to execute the case.

## Author
The code has been developed by Eleonora Gajetti. Contact email: egajetti@gmail.com
