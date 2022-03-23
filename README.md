# Citation Network: Link Prediction
The citation network is a graph where nodes are research papers and there is an edge between two nodes if one of the two papers cite the other. In addition to the graph structure, each node (i.e., article) is also associated with information such as the title of the paper, publication year, author names and a short abstract.

Edges have been deleted at random from this citation network. The objective is to accurately reconstruct the initial network using graph-theoretical, textual, and other information.

## Dataset
The initial dataset was provided in the following files:

- [node_information.csv](data/node_information.csv) : For each of the 27,770 nodes (papers), the file contains the (1) paper unique ID, (2) publication year (between 1993 and 2003), (3) title, (4) authors, (5) name of journal (not available for all papers), and (6) abstract. Abstracts are already in lowercase, common English stopwords have been removed, and punctuation marks have been removed except for intra-word dashes.
- [training_set.txt](data/training_set.txt) : The file contains the details of 615,512 labeled node pairs (1 if there is an edge between the two nodes, 0 else). One pair and label per row, as: source node ID, target node ID, and 1 or 0. The IDs match the papers in the node_information.csv file.
- [testing_set.txt](data/testing_set.txt) : This file contains the node pairs for which the prediction needs to be made. It has 32,648 node pairs. One pair per row, as: source node ID, target node ID.

In addition to these, other data files have been created by processing the provided information.

## Details of files

- [citation-network.ipynb](code/citation-network.ipynb) : Contains the final code
- [nodes.csv](data/nodes.csv) : Contains the details of nodes. Each row has the node ID, paper title.
- [edges.csv](data/edges.csv) : Contains the details of the edges. Each row has the source node ID, target node ID.