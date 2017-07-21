# Graph-Clustering
GRAPH CLUSTERING ALGORITHM in C++. The algorithm uses the Quality function by Girvan-Newman to implement the clustering.                

*quality function Q=(conn_edges(cluster1,cluster2)/m)-(dccluster[cluster1]*dccluster[cluster2])/(m*m);                  
where conn_edges(C1,C2) returns the number of connecting edges between cluster C1 and cluster C2. 
      dccluster[C1] stores the sum of degrees of each vertex in cluster C1.                  
**STEPS**

1)Initially, each vertex is itself a cluster.

2)At every step, two clusters C1 and C2 which have the highest Q value are merged.

3)Step 2 is repeated till Q value for any two clusters is positive.

#By default, the algorithm is run on the graph given in the image. 
