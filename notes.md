

## On Graph partitioning

**Using Knauer and Ueckerdt terminology**

host-graph: the overall graph with no "dangling" nodes
template: a specific sub-graph with potential constraints applied to it

Grouping prosumers to possible transformers is a graph partitioning problem:
https://en.wikipedia.org/wiki/Graph_partition

Specifically we are interested in a tree (or rooted) graph portioning. These 
algorithms ensure that each template of a host-graph contains exactly one of the
roots.

[Lit Review - Graph partitioning](https://www.sciencedirect.com/science/article/pii/S0012365X22000905)

"A rooted covering problem requires that every template contains the single root vertex or, in case of multiple given roots, that every template includes a distinct root vertex."


[Power Grid Partitioning](https://ieeexplore.ieee.org/document/10855832)

They also developed the modularity Q metric, which measures the performance of a network partition (Maybe interesting for measuring performance of parition)?

#### Fluid based partitioning

[NetworkX algorithm](https://networkx.org/documentation/stable/reference/algorithms/generated/networkx.algorithms.community.asyn_fluid.asyn_fluidc.html#r8f732acc89d3-1)

[paper](https://arxiv.org/pdf/1703.09307)

### Measure num. swtichstates

Use upper estimate of `2^(switchstates)` and then take random switch state. Count how many of these switch states adhere to the criteria (one trafo per grid, all components connected). Thus `relevant_switchstates = 2^(switchstates) * p_relevant_switchstate`


