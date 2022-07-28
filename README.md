# CQDistance

 easy to get the distance between CQDs after Molecular Dynamics Simulation 



---

These python scripts were created to get the distance easily between CQDs during MD simulation.

## How to use

- The input file should be a standard Gromacs output pdb, you should turn the md out file to be a PDB file. You can do this by the gmx command like this:
  
  `gmx trjconv -f out.xtc -s out.tpr -o output.pdb -pbc mol`

- 
