# 《Exploring Multi-granularity Contextual Semantics for Fully Inductive Knowledge Graph Completion》

Abstract: 

Fully inductive knowledge graph completion (KGC) aims to predict triplets involving both unseen entities and relations. Recent several approaches transform paths between entities into descriptions and modeling semantic correlations between paths using pre-trained language models (PLMs), have emerged as a promising solution for fully inductive reasoning. However, these methods often adopt a simplistic concatenation strategy for path-to-sentence transformation, which impedes PLMs' ability to capture subtle nuances in context, resulting in sub-optimal path context embeddings. Furthermore, they ignore the high-order semantics underlying the complete context, which can provide richer information for inductive reasoning. To address these issues, we propose a Multi-Granularity Contextual Semantic (MGCS) modeling framework, utilizing a Path Modeling Network (PMN) and a Subgraph Modeling Network (SMN) to extract two granularity levels of contextual semantics from single paths and complete subgraphs, for fully inductive KGC. The PMN extracts paths between head and tail entities and employs reasoning patterns from similar cases to filter out unreliable paths. Then two innovative path conversion strategies are designed to significantly enhance the pre-trained language model's understanding of specific path contexts. The SMN employs a neighbor interactive graph neural network to extract high-order semantics from the complete subgraph context with a concept-enhanced relation encoding, and optimizes it through a contrastive learning method. Finally, the confidence of the triples is evaluated from the perspective of global complete context by comparing the semantics between the subgraphs surrounding the target triplet and the subgraphs surrounding similar cases. Experimental results on benchmark datasets demonstrate the effectiveness of MGCS. 




## Dependencies:
The code is based on Python 3.7. In addition, you need to add the following dependencies to your environment：
- [huggingface transformer 3.3.1](https://github.com/huggingface/transformers)
- [pytorch 1.5.0](https://pytorch.org/)
- networkx 2.5
- tqdm
- colorama 0.4.4
- matplotlib 3.3.4
- numpy
- sklearn
- ipdb
- transformers 4.18.0

## Code structure

In the root directory, the “Data” folder contains all the data sets used in this work.

### How to train
Please change to the Code directory, and then use the following command to train the model.

Train WN18RR dataset using the following commands:

```shell script
python train.py -d WN18RR 

```

### How to evaluate 

Taking WN18RR as an example, use a command similar to the following to evaluate the model:

```shell script
python test.py -d WN18RR_ind

```


## Baselines
We use code provided by authors for baselines in our experiments.
RuleN is a ruled-based method. Detailed instructions can be found [here](http://web.informatik.uni-mannheim.de/RuleN/).
GraIL is subgraph reasoning method. Detailed instructions can be found [here](https://github.com/kkteru/grail).

## Acknowledgement
We refer to the code of some works ([GraIL], etc.) Thanks for their contributions.

More details can be found in the code. If you have any questions please contact us.
