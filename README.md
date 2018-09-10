# RelComp

Xiangyu Ke, Arijit Khan, and Leroy Lim Hong Quan 

Nanyang Technologicial University, Singapore

The RelComp project provides experimental comparison of 6 state-of-the-art s-t reliability estimators over uncertain graphs.

1. Check List:
	(1) RelComp.out : Executable program
	(2) RelComp.sln : Visual Studio 2017 solution file for RelComp project
	(3) RelComp.zip : Compressed source codes of RelComp project
	(4) lastfm/NetHept/dblp02/dblp005.zip : Datasets, including the original graph and 100 random queries. For lastfm and NetHept, we also provide the ProbTree indexes since they are small. For other datasets, one can generate the indexes locally with our program.

2. How to Compile:
	This work is created and organized as a Linux project with Visual Studio 2017. It adopts g++-5 -std=c11 compiler and relies on BOOST C++ library. Please refer to RelComp.sln for detailed setting.

3. How to Run:
	The command of running our program is "./RelComp.out [address]". The address stands for the path where the graph and queries are stored. Then our program will guide you to select the files to read and choose the algorithms for evaluation.

	Example: 
	(1) Type in "./RelComp.out ./lastfm"
	(2) Select "4. Load graph from file", then choose "2 -/lastfM.txt"
	(3) Choose "4. Find Optimal K for Monte Carlo Sampling (BFS)"
	(4) Choose Source-Target file, we select "1 -/lastfm_sourcetarget.txt"
	(5) The evaluation starts

4. The Description of Output Files:
	(1) Result files: [Dataset Name]_[Method Name]_[index].csv
		The Index here means that this file is for No.Index query.
		Each line in such file is organized as: [K],[Reliability],[Time(ms)],[Memory[B]]
	(2) Variance file: [Dataset Name]_[Method Name]_[Variance].csv
		Each line in such file is organized as: [K],[Variance],[_],[Index]
