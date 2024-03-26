[![INFORMS Journal on Computing Logo](https://INFORMSJoC.github.io/logos/INFORMS_Journal_on_Computing_Header.jpg)](https://pubsonline.informs.org/journal/ijoc)

# Exact and Approximation Algorithms for Sparse PCA (SPCA)

This archive is distributed in association with the [INFORMS Journal on Computing](https://pubsonline.informs.org/journal/ijoc) under the [MIT License](https://github.com/INFORMSJoC/2022.0372/blob/master/LICENSE).

The software and data in this repository are a snapshot of the software and data that were used in the research reported on in the paper [Exact and Approximation Algorithms for Sparse PCA (SPCA)](https://doi.org/10.1287/ijoc.2022.0372) by Yongchun Li and Weijun Xie.

## Cite

To cite the contents of this repository, please cite both the paper and this repo, using their respective DOIs.

https://doi.org/10.1287/ijoc.2022.0372

https://doi.org/10.1287/ijoc.2022.0372.cd

Below is the BibTex for citing this snapshot of the respoitory.

```
@article{li2020exact,
  title =     {Exact and approximation algorithms for sparse PCA},
  author =    {Li, Yongchun and Xie, Weijun},
  publisher = {INFORMS Journal on Computing},
  year =      {2024},
  doi =       {10.1287/ijoc.2022.0372.cd},
  url =       {https://github.com/INFORMSJoC/2022.0372},
  note =      {Available for download at https://github.com/INFORMSJoC/2022.0372},
}  
```

## Installation and set up
In order to run this software, you must install Gurobi 9.5.2 from https://www.gurobi.com/downloads/gurobi-software/ and MOSEK 10.0.29 from https://www.mosek.com/downloads/list/10/.

## Exact algorithms

We propose three equivalent mixed-integer convex programs to solve SPCA to optimality, denoted by MISDP (6), MISDP (15), and MILP (22) in our paper. The implementations of these exact formulations can be found in the "src" directory.

To be specific, we design a branch-and-cut algorithm with the closed-form cuts to solve MISDP (6), and the implementation is available in the "Branchandcut.py" file.

We also customize a branch-and-cut algorithm to solve MISDP (15), and the implementation is available in the "Branchandcut_15.py" file.

For MILP (22),  the implementation is available in the "MILP.py" file.

Lastly, we use the solver Gurobi 9.5.2 to directly solve the SPCA, and the implementation is available in the "spca_gurobi.py" file.

## Approximation algorithms

We investigate two approximation algorithms for solving SPCA: greedy and local search algorithms, and compare them with the existing truncation algorithm, randomized algorithm, and SDP-based algorithm. The implementations can be found in the "src" directory.

To be specific, the implementations of truncation, randomized, greedy, and local search algorithms can be found in the "lower_bounds.py" file.

The implementation of SDP-based algorithm is available in the "spca_sdp.py" file.

## Continuous relaxations

We propose three SDP continuous relaxations which provide different upper bounds for SPCA, denoted by SDP relaxation (8), SDP relaxation (13),  and SDP relaxation (16) in our paper. The implementations of these continuous relaxation can be found in the "src" directory.

To be specific, the implementations of SDP relaxation (8) is available in the "sdp_rels.py" file.

The implementations of SDP relaxation (13) is available in the "sdp_rel_thirteen.py" file.

The implementations of SDP relaxation (16) is available in the "sdp_rels.py" file.

Lastly, we compare the proposed SDP relaxations with SDP relaxation (17) whose implementation is also available in the "sdp_rels.py" file.

## Data

The ten UCI datasets used for the numerical study are available at https://github.com/maryami66/uci_dataset/tree/main, https://github.com/treforevans/uci_datasets, where the dimension spans from 13 to 128.

The matrices $A$ generated from UCI datasets are contained in the "data" directory. The other datasets used for the numerical study are also contained in the "data" directory.

## Reproduce numerical results

To reproduce each table in the paper, please run the file with corresponding table number in the "src" directory. For example, to generate table 2, please run ```python src/table2_gen.py```.

## Support

For support in using this software, submit an
[issue](https://github.com/INFORMSJoC/2022.0372/issues/new).
