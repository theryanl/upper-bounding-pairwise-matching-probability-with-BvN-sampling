This directory contains functions and commands necessary to re-run the experiments in the paper. 

The data/ subdirectory contains for convenience the correctly-formatted .npz files for the datasets we use for the experiments. The icml2018.npz file is sourced directly from https://github.com/xycforgithub/StrategyProof_Conference_Review. The preflib .npz files are constructed using the preflib_to_npz.py file, from the .toi files sourced directly from PrefLib dataset MD-00002 (http://www.preflib.org/data/matching/csconf/).

The baseline_algo/ subdirectory contains files used to run a baseline assignment algorithm not used in the paper.

The experiments in the paper can be re-run with the following commands (each of which save .npy files of the output data):
	- python testrunnerA.py data/iclr2018.npz 0 6 3
	- python testrunnerA.py data/preflib1.npz 0 6 3
	- python testrunnerA.py data/preflib2.npz 0 7 3
	- python testrunnerA.py data/preflib3.npz 0 6 3
	- python testrunnerA.py data/iclr2018.npz 1 6 3
	- python testrunnerA.py data/preflib1.npz 1 6 3
	- python testrunnerA.py data/preflib2.npz 1 7 3
	- python testrunnerA.py data/preflib3.npz 1 6 3
	- python testrunnerB.py 0.5 3 3 500 5000 500
	- python testrunnerC.py data/iclr2018.npz 6 3 15
	- python testrunnerC.py data/iclr2018.npz 6 3 811
	- python testrunnerC.py data/preflib1.npz 6 3 11
	- python testrunnerC.py data/preflib2.npz 7 3 8
	- python testrunnerC.py data/preflib3.npz 6 3 48
	- python testrunnerD.py
	- python test_runtime.py
	- python testrunnerE.py 3
	- python testrunnerE.py 6
	- python testrunnerE.py 9
	- python testrunnerE.py 12
	- python testrunnerF.py
Once run, the results in the files can be plotted with the appropriate call to plot_results.py.