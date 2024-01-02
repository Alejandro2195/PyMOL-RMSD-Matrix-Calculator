# PyMOL-RMSD-Matrix-Calculator
This Python code utilizes the PyMOL module to calculate and generate a Root Mean Square Deviation (RMSD) matrix between protein structures in PDB format

Importing necessary libraries and modules:

    argparse: Used for handling command-line arguments (although it is commented out and not used in this code).
    os, sys, glob: Used for operations related to the operating system and file manipulation.
    numpy (as np): Used for numerical operations and matrix manipulation.
    pymol.cmd: Provides access to PyMOL functions for loading and manipulating protein structures.

Definition of functions:

    rootname(filename): Extracts the base name of a file by removing the extension, especially if it is a compressed file (.gz).
    write_csv(filename, unique_files, mat): Writes an RMSD matrix in CSV format.
    write_meg(filename, unique_files, mat): Writes an RMSD matrix in Mega-compatible format.

Definition of the main function main(argv):

    Comments out the creation of an argparse.ArgumentParser object and the definition of command-line arguments.
    Uses easydict to simulate an argument object, as the argparse part is commented out.
    Retrieves the list of PDB files in a specific folder.
    Initializes an rmsd_mat matrix to store RMSD values between structures.
    Uses PyMOL to load structures and calculate RMSD between them.
    Calls the write_csv and write_meg functions to write the results in CSV and Mega files, respectively.

Script execution:

    Loads PDB structures one by one and calculates RMSD between them.
    Ignores structures that cannot be loaded correctly and sets the corresponding values in the matrix to -1.0.
    Writes the results in CSV and Mega files.

The script searches for PDB files in a specific folder, loads the structures using PyMOL, calculates RMSD between them, and stores the results in matrices and output files. It is important to have PyMOL installed and configured correctly for the script to function properly.
**IMPORTANT: Please change pdb_files = glob.glob(r'PDB\FOLDER\*.pdb') to the folder where the pdb files are located
