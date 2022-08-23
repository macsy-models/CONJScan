# CONJScan models - Models for detection of conjugative, decayed conjugative and mobilisable elements

This set of MacSyFinder's models are dedicated to the detection of conjugative, decayed conjugative and mobilisable elements.

The conjugative T4SS that can be detected are:

- T4SS_typeG
- T4SS_typeF
- T4SS_typeC
- T4SS_typeB
- T4SS_typeI
- T4SS_typeT
- T4SS_typeFA
- T4SS_typeFATA

Mobilisable elements detected will be described as:

- MOB

Decayed conjugative T4SS will be described as:

- dCONJ_typeG
- dCONJ_typeF
- dCONJ_typeC
- dCONJ_typeB
- dCONJ_typeI
- dCONJ_typeT
- dCONJ_typeFA
- dCONJ_typeFATA

CONJScan now includes two sets of models. One is specific to the detection of conjugative, decayed conjugative and mobilisable elements in chromosomes and the second to the detection in plasmids. They are compatible with **MacSyFinder version 2**.

## Installation and Usage with MacSyFinder

First, the `macsyfinder` program should be [installed](http://macsyfinder.readthedocs.io/en/latest/). This will also install the `macsydata` tool that enables to easily install this package of MacSyFinder models from this repository.


The basic commands to run are then:

    macsydata install CONJScan


to install the CONJScan package.

    macsyfinder --db-type ordered_replicon \
		--sequence-db myproteins.fasta \
		--models CONJScan/Plasmids system --option 		


to run the search on your favorite organism's **Plasmids**, where `system` is one or multiple systems listed above, or `all` to search for all the above listed systems
(see [MacSyFinder's documentation](http://macsyfinder.readthedocs.io/en/latest/)).


    macsyfinder --db-type ordered_replicon \
		--sequence-db myproteins.fasta \
		--models CONJScan/Chromosome system --option 		


to run the search on your favorite organism's **Chromosome**, where `system` is one or multiple systems listed above, or `all` to search for all the above listed systems
(see [MacSyFinder's documentation](http://macsyfinder.readthedocs.io/en/latest/)).


It has to be noted that the models were designed to be used accordingly to the replicon type. Plasmids models should be used for plasmids typing and Chromosome models should be used for chromosomes. Complete models (T4SS_typeB, T4SS_typeC, T4SS_typeF, T4SS_typeG, T4SS_typeI, T4SS_typeT, T4SS_typeFA, T4SS_typeFATA) can be used alone. However, we strongly recommend that you use **all** systems in each package (/Chromosome or /Plasmids) at once.


## References

- Jean Cury, Marie Touchon, Eduardo P. C. Rocha,
  Integrative and conjugative elements and their hosts: composition, distribution and organization.
  Nucleic Acids Research, Volume 45, Issue 15, 6 September 2017, Pages 8943–8956.
  [doi: 10.1093/nar/gkx607](https://doi.org/10.1093/nar/gkx607)
