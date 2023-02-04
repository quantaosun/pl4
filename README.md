# pl4

a represents a two-dimensional compound without a specific three-dimensional structure, which has the specificity of the chemical structure. *a* represents a compound with a specific three-dimensional conformation and its coordinates. If the three-dimensional conformation changes, we will record the new structure as a'. If there are multiple The conformation is recorded as [a]. And we assume that the binding conformations of a and b in the target pocket can be superimposed.

The process is:

A protein-chemical molecule binding complex p-a obtained by docking
By kinetically optimizing p-a, we get p'-a'
Modification of a' is mainly to add a small substituent at the position of the H atom to obtain a new molecule b, and sample the conformation of b to obtain [b]; perform a preliminary score on [b], which integrates CNN or machine learning The scoring function to find a better scoring b'
Use the free energy perturbation with high computational cost to further verify the difference in the binding free energy of a' and b', and decide whether to synthesize b.

- pl3 docking to obtain an initial docked complex, ```output.pdb``` and ```Docked1.pdb```
- Making-it-rain MD to optimise the docked pose
- Fegrow to design new analogues and score with CNN powered Ginia

5XV7 + XEY smiles, validated

### Step 1
docking

### Step 2
molecular dynamics

### Step 3
new analogues design

