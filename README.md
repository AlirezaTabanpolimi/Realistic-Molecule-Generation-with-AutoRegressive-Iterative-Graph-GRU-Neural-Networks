# Realistic-Molecule-Generation-with-Iterative-AutoRegressive-Graph-GRU-Neural-Networks
Development of Graph GRU Autoregressive Generative Neural Network for Generating realistic molecules of different size from Scratch with TensorFlow.( based on the paper by prof .Jure Leskovec ).                                      
In this ongoing project , I created data generator that each time its called it does a BFS tree on randomly chosen nodes from each graph in a batch of graphs ,                                                               
 then based on these orderings it transforms the adj matrix of each graph to a sequence of sequences and masks the graphs ,
The  model I have developed is an Autoregressive custom model with Node-Level and edge level multi  GRU_cells layer in custom loops that cooperatively learn the iterative dynamics of creation of Graphs in the batch 
with teacher forcing , also the node level GRUs have another output to learn the EOS . Based on the trained layers , In test, Model continues the grow process of the graph till the EOS token is one .
