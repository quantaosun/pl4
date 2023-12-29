# pl4

## A collection of notebooks for cloud docking, simulation and designing new medicinal analogues.

Assume *a* represents a two-dimensional compound without a specific three-dimensional structure, which has the specificity of the chemical structure. While **a** represents a compound with a specific three-dimensional conformation and its coordinates. If the three-dimensional conformation changes, we will record the new structure as **a'**. If there are multiple The conformation is recorded as **[a]**. We assume that the binding conformations of a and b in the target pocket can be superimposed.

The process is:

- 1.A protein-chemical molecule binding complex p-a obtained by docking (updated docking method to quantaosun/labodock_binder)
- 2.By kinetically optimizing **p-a**, we get **p'-a'**
- 3.Modification of **a'** is mainly to add a small substituent at the position of the H atom to obtain a new molecule **b**, and sample the conformation of **b** to obtain **[b]**; perform a preliminary score on **[b]**, which integrates CNN or machine learning The scoring function to find a better scoring **b'**

Updated fegrow build command to 

```
rmols = fegrow.build_molecules(template_mol,  
                               selected_rgroups,
                              attachment_index)
```

originally

```
rmols = fegrow.build_molecules(template_mol,  
                              attachment_index,
                              selected_rgroups)
```


- 4. Use the free energy perturbation with high computational cost to further verify the difference in the binding free energy of **a'** and **b'**, and decide whether to synthesize b.





