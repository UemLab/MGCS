# 《Exploring Multi-granularity Contextual Semantics for Fully Inductive Knowledge Graph Completion》
## Authors: Jingchao Wang, Weimin Li, et al.


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

## Structure

In the root directory, the “data” folder contains all the data sets used in this work.

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



## Acknowledgement
We refer to the code of some works ([GraIL], etc.) Thanks for their contributions.

More details can be found in the code. If you have any questions please contact us.
