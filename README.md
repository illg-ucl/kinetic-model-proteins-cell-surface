# kinetic-model-proteins-cell-surface

Kinetic modeling of cell-surface receptor proteins, including receptor-ligand binding, receptor dimerization, endocytosis and recycling. Mathematica notebook (Mathematica 11.0 version).

**Related publication (academic paper)**: Critical roles for EGFR and EGFR-HER2 clusters in EGF binding of SW620 human carcinoma cells, Adam J. M. Wollman, Charlotte Fournier, Isabel Llorente-Garcia, Oliver Harriman et al., Journal R. Soc. Interface, 19: 20220088 (2022). https://royalsocietypublishing.org/doi/10.1098/rsif.2022.0088. 

# Copyright and License

Copyright (c) 2019. Isabel Llorente Garcia.

Released and licensed under a BSD 2-Clause License:

https://github.com/illg-ucl/kinetic-model-proteins-cell-surface/blob/main/LICENSE

This program is free software: you can redistribute it and/or modify
it under the terms of the BSD 2-Clause License.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
BSD 2-Clause License for more details. You should have received 
a copy of the BSD 2-Clause License along with this program. 

If you use this software for your data analysis please acknowledge 
               it in your publications and cite as follows.
               
               - Citation example 1: 
               kinetic-model-proteins-cell-surface. (Version). 2019. Isabel Llorente Garcia, 
               https://github.com/illg-ucl/kinetic-model-proteins-cell-surface. (Download date).
               
               - Citation example 2:
               @Manual{ ,
                title  = {kinetic-model-proteins-cell-surface. (Version).},
                author       = {{Isabel Llorente Garcia}},
                year         = 2019,
                url          = {https://github.com/illg-ucl/kinetic-model-proteins-cell-surface}
               }

# Description of the model

A brief description of the model can be found in the pdf file **"suppl_info_published_paper_2022.pdf"**, in pages 10-14 under the heading "*Kinetic modeling of EGFR ligand binding, dimerization, endocytosis and recycling*". See also figures S10 and S11 in the same document, in pages 22 and 23. This document is part of the above-mentioned published academic paper, it is the Supplementary Information.

Additionally, the pdf file **"CooperativeBinding_EGFR_Aug2019.pdf"** is a copy of the Mathematica Notebook with all the detailed explanations and outputs.

A **Mathematica notebook file (.nb)** with all outputs can be provided upon request (it is a large 27.5 MB file with outputs that I cannot upload here as it is too large, and which I cannot modify to remove outputs as I no longer have a Mathematica License). 

The model is a multi-state time-dependent kinetics model for ligand binding to receptor monomers and dimers, incorporating homo- and hetero-dimerization of ligated and unligated receptors, internalization of ligated receptors via endocytosis and subsequent recycling of receptors to the plasma membrane. 

Notation: R for receptor monomers (EGFR), RR for receptor dimers, L for EGF ligand, RL for ligated receptor monomers, RRL for singly-ligated receptor dimers, RRL2 for doubly-ligated receptor dimers, RL_inside for endocytosed RL, RRL_inside for endocytosed RRL and RRL2_inside for endocytosed RRL2.

The model solves multiple rate equations to determine concentrations of ligated and unligated receptor monomers and dimers, and concentrations of internalized receptors, as a function of time. The model considers reversible reactions for ligand binding and receptor dimerization. It considers only endocytosis of ligated receptors (RL, RRL, RRL2) and, in the first instance, it assumes that recycling returns unligated receptors to the plasma membrane. It assumes the same endocytosis and recycling rates for all reactions. 

Considering all relevant reactions, a system of simultaneous rate equations is written for the concentrations of all species as a function of time and corresponding reaction rates. The total concentration of receptors on the cell membrane is imposed as a constraint. The system of equations is solved with relevant initial conditions (e.g. all ligated and internalised components are zero at time=0, relevant experimentally observed values) and relevant experimental rate constants for all reactions (see details in the above document). 

The solution of the system of equations returns the concentrations of ligated/unligated/endocytosed monomer and dimerized receptor proteins as a function of time. Additionally, the model calculates the fractional saturation on the cell surface, equal to the ratio of ligand to receptor molecules (ligand:receptor ratio) on the plasma membrane. These modelled values can be compared to experimentally measured values on living cells (measured via fluorescence microscopy), particularly to equilibrium values.

![fig_S10](https://github.com/illg-ucl/kinetic-model-proteins-cell-surface/assets/17204635/7c6d1e0d-a487-41f3-9708-140b664d9d76)

---

![fig_S11](https://github.com/illg-ucl/kinetic-model-proteins-cell-surface/assets/17204635/856e78c3-66a4-47c3-8f62-b93d58cf54ea)
