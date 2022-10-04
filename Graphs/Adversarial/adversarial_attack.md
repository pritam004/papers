## 1. Graph Structure Learning for Robust Graph Neural Networks(2020,SIGKDD)

problem stement : Provide defensive solution against adversarial attacks on graphs.

Important reference :
metattack (adversarial attacks on neural networks for graph data)
netattack
RL-S2V(reinforcement learning attack against GNNs) ICML,2018 

solution idea:

1. To recover the clean graph structure from the noisy and perturbed graph, one potential way is to learn a clean adjacency matrix 
S close to the adjacency matrix of the poisoned graph by introducing the new adjacency matrix with the properties of low rank and sparsity.

2. Rank decreases much faster by removing adversarial edges instead of normal edges. Ensures  sparsity and low rank of graphs.

3. Feature smoothness: Neighbouring nodes have similar properties. Takes squared error on the node attributes for every edge as a loss.

4. Alternate training including the two losses. Generating clean graph 1st phase and trainig on it in the next phase.

Rating and Review : 4/10

One of the initial works in the field of defence against adversarial attacks. The proposed method is heuristic in nature but works good in practice
as shown by authors. Code released by authors.
