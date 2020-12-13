# Bonding number of social graphs

**Introduction:** <br /> 

Bonding number(d) is the smallest integer ‘d’ such that every person staying in touch with at least ‘d’ others guarantees the connectivity of the group.

We want to find lower bounds on the bonding number. The following is a simple strategy based on clustering:
1. Find a clustering of the graph G.
2. For each cluster Ci, let Hi be the disconnected graph formed by deleting edges between Ci and the rest of G.
3. Find the maximum value of d such that some Hi is d-bonded.
4. Output d + 1 as a lower bound on τ (G).

As we can see, a major part of the solution demanded clustering the graph. 
I implemented the Girvan-Newman graph clustering algorithm from scratch. (code: clustering_shivam.cpp) 

**Girvan-Newman graph clustering algorithm:** <br />      
The algorithm uses the Quality function(Q) by Girvan-Newman to implement the clustering.      

 **Q=(conn_edges(cluster1,cluster2)/m)-(dccluster[cluster1]\*dccluster[cluster2])/(m\*m)**   <br />               
where, **conn_edges(C1,C2)** returns the number of connecting edges between cluster C1 and cluster C2. <br />  
      **dccluster[C1]** stores the sum of degrees of each vertex in cluster C1.   
      
**Steps employed in Girvan-Newman graph clustering algorithm:**<br />
1) Initially, each vertex is itself a cluster.<br />
2) At every step, two clusters C1 and C2 which have the highest Q value are merged.<br />
3) Step 2 is repeated till Q value for any two clusters is positive.

#By default, the code takes the graph given in the following image as input:

![alt text](https://github.com/shivam2296/Graph-Clustering/blob/master/sample.jpg)
