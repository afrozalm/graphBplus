# graphBplus
graphB+ is a balancing algorithm for signed social network graphs. It operates on graphs stored in CSV format. A sample input graph is available under graph.csv.

graphBplus_02.cu contains the CUDA code and graphBplus_02.cpp contains the OpenMP C++ code (with g++ intrinsics).

The CUDA code can be compiled as follows:

  nvcc -O3 -arch=sm_70 graphBplus_02.cu -o graphBplus

The OpenMP C++ code can be compiled as follows:

  g++ -O3 -march=native -fopenmp graphBplus_02.cpp -o graphBplus

To run the code on the input file graph.csv with 100 samples and save the results of the balanced solutions in out.csv, enter:

  ./graphBplus graph.csv 100 out.csv

This work has been supported in part by equipment donations from Nvidia Corporation.
