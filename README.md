# Geomagnetic Depth Sounding 3D Modeling and Inversion Program

## Introduction

This program is a set of F90 codes for Geomagnetic Depth Sounding 3D Modeling and Inversion, capable of performing three-dimensional forward and inverse calculations for geomagnetic depth sounding.

## Preparation

Before using the code, you need to install the Intel® oneAPI Base Toolkit and the Intel® HPC Toolkit.

## File Structure

The program mainly contains three folders: `lib`, `src`, and `vs`.

- `lib`: Contains the libraries required for the program to run, including the MUMPS solver, bisect, and TetGen libraries.
- `src`: The source code folder, containing subfolders such as Common, Data, Forward, Inverse, Main, Model, Primary, Solver, etc., with functionalities as indicated by their names.
- `vs`: Contains the Intel Fortran project file and examples.

### Example Files

- `*.ele` & `*.node`: The mesh files of the model, containing tetrahedral element information and node information, respectively, in TetGen format.
- `*.attribute`: Contains the relevant initial electrical information of the different regions after the model is partitioned.
- `*.ctrl`: Some control parameters of the algorithm need to be specified.
- `*.data`: For forward calculations, the data format needs to be specified; for inversion, observational data is required.
- `*.source`: Stores information about the source of the electromagnetic field.
- `task.dat`: Task information needs to be specified in advance.
-`newsedmap.txt`: It is the 180 x 360 surface conductance data from Everett, M.E., S. Constable, and C.G. Constable, 2003: Effects of near-surface conductance on global satellite induction responses, Geophys. J. Int., 153, 277–286.

### Output Files

- `*.o.data`: The output results of the forward calculations.
- `*.res`, `BFGS_rms_record.txt`, `*.vtk`: Main inversion results and related parameter files.

## Installation Guide

Ensure that the Intel® oneAPI Base Toolkit and Intel® HPC Toolkit are installed. For detailed installation steps, please refer to the official documentation.

## Usage

For detailed usage instructions and parameter configurations, please refer to the examples and `.ctrl` files in the `vs` folder.

## Contributions

Contributions via Pull Requests or by emailing maxp20@mails.jlu.edu.cn with code contributions or issues are welcome.

## Author

- **Name**: Xinpeng Ma
- **Affiliation**: Jilin University
- **Email**: maxp20@mails.jlu.edu.cn

## License

This code is distributed under the GPL License. For more details, please see the LICENSE file.
