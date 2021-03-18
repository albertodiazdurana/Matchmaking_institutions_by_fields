# Matchmaking_institutions_by_fields

Matchmaking of institutions described by a given number of features is determenid by the the nearest neighbors algorithm KNN. See https://scikit-learn.org/stable/modules/neighbors.html#nearest-neighbor-algorithms

 This Jupyter notebook generates a list of indices for each row (institution) based on KNN. This list is stored in a csv file when the notebook is run.
 
 The nearest neighbors algorithm KNN will idicate the closeness according to Eucleadean distance to the datapoint in observation.
 The observed datapoint is given in the output array in the first column. The neighbors of the observed datapoint are the consecutive columns of the array.
 
 This code has been written to find 5 neighbouring datapoints. This value can be changed to find other number of neighbors.
 
 
 How to read the results:
 
Let's assume the output array

[[  5   1   2   0  12]
 [  5   1   2   0  12]
 [  5   1   2   0  12]
 [  3  73  15  96  88]
 [  4  28  22  10   1]
 [  5   1   2   0  12]]
 
 Looking at the top row, the row 0 (the observed datapoint) is neighbor to the row 1, the row 2, the row 5, and the row 12.
 Looking at the following row, we notice that that it is the same as the top row, since the row 1 in neigbor to the row 0, the row 2, the row 5, and the row 12.
 Same happens with the row 2.
 Row 3 is neighbor to the row  73, the row 15, the row 96, and the row 88.
