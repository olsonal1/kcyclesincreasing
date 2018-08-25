
# A randomized python algorithm to detect small k-cycles in undirected graphs.
- by Alexander Olson

There is a relatively straightforward algorithm to find triangles in a graph, given its adjacency matrix A: by simply calculating A^2, and checking for a 1 at index (i, j) in A^2 and at index (j, i) in A, we can verify that there is a path of length 2 from i to j and a closing edge 
from j to i.

The general problem of, "can we find a k-cycle in an undirected graph?"- where k is an input parameter- has been proven to be NP-hard. However, by generalizing and randomizing the matrix multiplication algorithm as above, we can find k-cycles of length less than lg(n) in a close-to-polynomial O(n^w+lglg(n-1)), where w is the constant of matrix multiplication (less than 2.4 with the most efficient implementations): the algorithm works with a 98% probability of success.

You can find a fuller analysis of the algorithm's correctness, accuracy and runtime in "kcyclesincreasing.pdf".

If you'd like to use this code for any (non-plagiarizing reason), feel free! (But please attribute it).
