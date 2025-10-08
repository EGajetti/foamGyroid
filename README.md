# foamGyroid
Example of simulation setup in OpenFOAM to mesh a single periodic cell of a TPMS, then simulate it using periodic hydraulic and thermal boundary conditions.

## Software and general requirements
The case was developed and tested in [OpenFOAM v2212](https://www.openfoam.com/download/release-history#v2212).
In the folder ```constant/triSurface``` a geometry must be inserted, in .stl format, with dimension 10x10x10 (possbly larger to avoid problems when cut in blockMesh).
Within ```system/controlDict``` and ```system/controlDictScalar``` two custom function objects are used, that you might find in the submodules ```myFO```. If you do not want to compile them, you can just comment them within the controlDict files.

## Usage
In ```0.orig/T``` and ```0.Tw/T``` you can find two different implementations of the thermal periodic boundary conditions as codedFixedValue, depending on wheter the wall heat flux or the wall temperature are prescribed, sa described in [1].

Run the ./Allrun file to execute the case.

[1] F.P. Incropera, D.P. Dewitt, T.L. Bergman and A.S. Lavine. Fundamentals of Heat and Mass Transfer, sixth edition. John Wyley & sons, 2007.

## Author
The code has been developed by Eleonora Gajetti. Contact email: egajetti@gmail.com
