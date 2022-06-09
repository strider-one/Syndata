# Syndata
## Network visualization using Python-NetworkX

### Run 'dependencies.py' before first run to initialize the required modules and directories

### Application:
#### Run the scripts in following order:
>1. Run **connection_list_generator / matrix_generator** to first generate either an edgelist or a matrix
>2. Then run **connection_to_graph_matrix / matrix_to_graph_list** to convert to an adjacency matrix and a networkx graph
>3. After that run **automated_elbow_method / silhoutte_method** to find the optimal number of clusters.
>4. Next run **embedder_graphviz / embedder_node2vec** to convert to a dimensionally efficient object
>5. Finally run **clustering_graphviz / clustering_node2vec** to visualize the clusters in a networkx graph.

### Files and their usages:
#### Data generation and Conversion
>##### 1. connection_list_generator.py
>For generating random edgelist. Can be used for drawing NetworkX graphs and converting to Numpy adjacency matrix.

>##### 2. connections_to_graph_matrix.py
>For converting edgelist generated from "connection_list_generator.py", to Numpy adjacency matrix and NetworkX graph.

>##### 3. matrix_generator.py
>For generating random adjacency matrix. Can be used for drawing NetworkX graphs and converting to edgelist.

>##### 4. matrix_to_graph_list.py
>For converting adjacency matrix generated from "matrix_generator.py", to edgelist and NetworkX graph.

>##### 5. syndata_generator.py
>For generating synthetic data, containing Location, Gender, Age, Education.

#### Optimal number of clusters
>##### 1. automated_elbow_method.py
>For automatically finding out optimal number of clusters, using elbow method from the edgelist generated by NetworkX, and supplying it to clustering files (sklearn, yellowbrick).

>##### 2. elbow_method_for_k.py
>For manually finding out optimal number of clusters, using elbow method from the edgelist generated by NetworkX (sklearn, scipy).

>##### 3. silhoutte_method_for_k.py
>For automatically finding out optimal number of clusters, using silhoutte method from the edgelist generated by NetworkX, and supply it to clustering files (sklearn).

#### Embedding and Clustering
>##### 1. embedder_graphviz.py
>For embedding nodes to graph-vector space using Graphviz (NetworkX).

>##### 2. embedder_node2vec.py
>For embedding nodes to 2-dimension space using Node2vec.

>##### 3. cluster_graphviz.py
>For clustering the nodes using Graphviz (NetworkX), with number of optimal clusters generated from either elbow or silhoutte method, and embedding of the nodes from "embedding.emb" and position of nodes from "positions.pkl".

>##### 4. cluster_node2vec.py
>For clustering the nodes using Node2vec, with number of optimal clusters generated from either elbow or silhoutte method and embedding of the nodes from "embedding.emb".

#### Other files
>##### 1. connections_generated.csv
>Random edgelist generated by "connection_list_generator.py".

>##### 2. connections_exported.csv
>Edgelist generated by converting adjacency matrix ("matrix_generated.csv") using "connections_to_graph_matrix.py".

>##### 3. matrix_generated.csv
>Random adjacency matrix generated by "matrix_generator.py".

>##### 4. matrix_exported.csv
>Adjacency matrix generated by converting edgelist ("connections_generated.csv") using "matrix_to_graph_list.py".

>##### 5. db_connections.csv
>Static database of edgelist for common use/testing.

>##### 6. db_matrix.csv
>Static database of adjacency matrix for common use/testing.

>##### 7. list2graph.png
>NetworkX graph generated by edgelist.

>##### 8. matrix2graph.png
>NetworkX graph generated by adjacency matrix.

>##### 9. edgelist.txt
>Similar to "connections_exported.csv", used in finding out optimal number of clusters and clustering methods.

>##### 10. embedding.emb
>Contains embedding information of nodes, for both Graphviz and Node2vec methods.

>##### 11. positions.pkl
>Contains node positions generated by Graphviz embedder.

>##### 12. optimal_clusters.txt
>Contains optimal number of clusters, used by clustering code (both Graphviz and Node2vec)

>##### 13. dumped.csv
>Contains synthetic data of Location, Age, Gender, Education

>##### 14. graph.xlsx
>Contains Location vs Age graph
