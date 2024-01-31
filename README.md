# Exact and Approximation Algorithms for Sparse PCA (SPCA)
This archive is distributed in association with the [INFORMS Journal on Computing](https://pubsonline.informs.org/journal/ijoc) under the [MIT License](https://github.com/INFORMSJoC/2019.0000/blob/master/LICENSE).

The software and data in this repository are a snapshot of the software and data that were used in the research reported on in the paper [Exact and Approximation Algorithms for Sparse PCA](https://optimization-online.org/wp-content/uploads/2020/05/SPCA_online-1.pdf) by Yongchun Li and Weijun Xie.

## Cite

## Exact algorithms
We propose three equivalent mixed-integer convex programs to solve SPCA to optimality, denoted by MISDP (6), MISDP (15), and MILP (22) in our paper. The implementations of these exact formulations can be found in the "src" directory.


To be specific, we design a branch-and-cut algorithm with the closed-form cuts to solve MISDP (6), and the implementation is available in the "Branchandcut.py" file.\
We also customize a branch-and-cut algorithm to solve MISDP (15), and the implementation is available in the "Branchandcut_15.py" file.\
For MILP (22),  the implementation is available in the "MILP.py" file.\
Lastly, we use the solver Gurobi 9.5.2 to directly solve the SPCA, and the implementation is available in the "spca_gurobi.py" file.


## Approximation algorithms
We investigate two approximation algorithms for solving SPCA: greedy and local search algorithms, and compare them with the existing truncation algorithm, randomized algorithm, and SDP-based algorithm. The implementations can be found in the "src" directory.


To be specific, the implementations of truncation, randomized, greedy, and local search algorithms can be found in the "lower_bounds.py" file.\
The implementation of SDP-based algorithm is available in the "spca_sdp.py" file.

## Continuous relaxations
We propose three SDP continuous relaxations which provide different upper bounds for SPCA, denoted by SDP relaxation (8), SDP relaxation (13),  and SDP relaxation (16) in our paper. The implementations of these continuous relaxation can be found in the "src" directory.


To be specific, the implementations of SDP relaxation (8) is available in the "sdp_rels.py" file.\
The implementations of SDP relaxation (13) is available in the "sdp_rel_thirteen.py" file.\
The implementations of SDP relaxation (16) is available in the "sdp_rels.py" file.\
Lastly, we compare the proposed SDP relaxations with SDP relaxation (17) whose implementation is also available in the "sdp_rels.py" file.

## Data
The ten UCI datasets used for the numerical study are available at https://github.com/maryami66/uci_dataset/tree/main, https://github.com/treforevans/uci_datasets, where the dimension spans from 13 to 128.\
The matrices $A$ generated from UCI datasets are contained in the "data" directory. The other datasets used for the numerical study are also contained in the "data" directory.

## Reproduce numerical results
To reproduce each table in the paper, please run the file with corresponding table number in the "src" directory.

# Thank you

Thank you for your interest in Sparse PCA (SPCA). Please let me know if you encounter any issues using this code, or have comments or questions. Feel free to email me anytime.

Yongchun Li ycli@gatech.edu
