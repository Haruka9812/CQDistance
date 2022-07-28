# CQDistance

 easy to get the distance between CQDs after Molecular Dynamics Simulation 



---

These python scripts were created to get the distance easily between CQDs during MD simulation.

For now,  CQDistance can only deal with CQD MD reasults producing by:

- Modeling by CDmaker (Paloncyova, M.;  Langer, M.; Otyepka, M., Structural Dynamics of Carbon Dots in Water and N, N-Dimethylformamide Probed by All-Atom Molecular Dynamics Simulations. J Chem Theory Comput 2018, 14 (4), 2076-2083. DOI: 10.1021/acs.jctc.7b01149 )

## How to use

- The input file should be a standard Gromacs output pdb, you should turn the md out file to be a PDB file. You can do this by the gmx command like this:
  
  `gmx trjconv -f out.xtc -s out.tpr -o output.pdb -pbc mol`

- Using `split_pdb` tool to split the pdb file as many files which everyone include pdb information in one flame and the filename will be the time point of this flame.
  
  - You can easily use `split_pdb` by run it in terminal, and make sure the following modules are installed in your enviroment.
    
    - optparse
  
  -  And the options of `split_pdb`:
    
    - `-f` path of input file, it should be a standard pdb file including all pdb information in all flames. Default is 'npt.pdb'. example: `-f cqd.pdb`
    
    - `-o` path to save the splited pdb files, it should be a Directory, and default is './split_all'. example: `-o ./cqd_split`
    
    - `-d` the time delta (ps) of every two flames in your pdb files. For example, if you run npt in dt = 0.002 (ps), nsteps = 25000000, nstlog = 10000. The time delta of this pdb file will be 0.002 * 10000 = 20 (ps), and you can appiont `-d 20`
  
  - 
