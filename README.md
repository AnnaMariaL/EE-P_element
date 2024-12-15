# README

This repository accompanies the following preprint: "Purifying Selection Shapes the Dynamics of P-element Invasion in Drosophila Populations"

This repository contains:
- time-resolved P-element CN estimates
- individual-based simulation models implemented in SLiM4
- simulation data
- trained GPs
- Jupyter notebooks demonstrating the usage of GPs 

# OVERVIEW

- **data/experimental-evolution/**: Contains the time-resolved P-element CN estimates for the 1st and 2nd wave experimental evolution study. 
gen = generation; replicate = evolutionary replicate ID, CN = P-element copy number estimate per haploid genome (software used: DeviaTE)

- **data/simulations/**: Contains simulated training (n=1,000), validation (n=5,000) , and test data (n=5,000) for surrogate modeling using Gaussian Processes. Simulations were run until the P-element was lost, or for 120 generations. Note that only evolved time-points that were sequenced in the empirical study were used for statistical emulation. GEN = generation;	trans_prob = transposition probability (*u* in manuscript); N_per_line	= number of flies used from each isofemale line to initialize the simulation (= 5); sel_alpha = alpha parameter of beta distribution determining selection coefficients for P-elements;	sel_beta = beta parameter of beta distribution determining selecfion  coefficients for P-elements;	l_pi = piRNA cluster size (scaled to percent (min = 0, max = 1) for Gaussian processes, *f_regulatory* in manuscript);	p_te = probability of isofemale line carrying the P-element (*p_carrier* in manuscript);	id = simulation ID;	q025 = 2.5th percentile of P-element copy number per haploid genome across *n* simulation runs;	q050 = median P-element copy number per haploid genome across *n* simulation runs;	m = mean P-element copy number per haploid genome across *n* simulation runs (used for Gaussian Process training);	q0975 = 97.5th percentile of P-element copy number per haploid genome across *n* simulation runs;	cv = coefficient of variation for P-element copy number per haploid genome across *n* simulation runs;	n = number of simulation runs conducted per parameter combination; 
- **src/IBM**: Contains individual-based models implemented in SLiM4 simulating P-element invasions in experimental *Drosophila simulans* populations. 
