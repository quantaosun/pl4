# pl4

a represents a two-dimensional compound without a specific three-dimensional structure, which has the specificity of the chemical structure. **a** represents a compound with a specific three-dimensional conformation and its coordinates. If the three-dimensional conformation changes, we will record the new structure as **a'**. If there are multiple The conformation is recorded as **[a]**. And we assume that the binding conformations of a and b in the target pocket can be superimposed.

The process is:

- 1.A protein-chemical molecule binding complex p-a obtained by docking
- 2.By kinetically optimizing **p-a**, we get **p'-a'**
- 3.Modification of **a'** is mainly to add a small substituent at the position of the H atom to obtain a new molecule **b**, and sample the conformation of **b** to obtain **[b]**; perform a preliminary score on **[b]**, which integrates CNN or machine learning The scoring function to find a better scoring **b'**

- 4.Use the free energy perturbation with high computational cost to further verify the difference in the binding free energy of a' and b', and decide whether to synthesize b.


- 1.pl3 docking to obtain an initial docked complex, outputs are ```output.pdb``` and ```Docked1.pdb```, i.e., p and a
- 2.Making-it-rain MD to optimise the docked pose,  outputs is prot_lig_prod_1.pdb, i.e., p' and a'
- 3.Fegrow to design new analogues and score with CNN powered Ginia, output is the best conformer of b,  i.e., b'
- 4. FEP simulation with third-party workflow



