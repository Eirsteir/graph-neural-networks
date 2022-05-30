# Graph Neural Networks Projects


This repository contains implementations of state-of-the art graph machine learning models for recommendations, link prediction and node classification:

1. [Movie recommendations with IGMC [1] (link prediction)](igmc-movie-recommendations.ipynb). Movies are recommended to users using only information from subgraphs.  
2. [Link prediction using SEAL [2]](seal-link-prediction.ipynb). Predict missing links in a citation network by using the SEAL framework.
3. [Node classification using HGT [3]](hgt-ogb-mag-node-classification.ipynb). Predict node properties in a heterogeneous graph. 

## Installation requirements
```
ogb>=1.3.0
torch>=1.11.0
pytorch-lightning>=1.2.0
torch-geometric==master (pip install git+https://github.com/rusty1s/pytorch_geometric.git)
```
Other required python libraries include: numpy, scipy, tqdm etc. These are found in [requirements.txt](requirements.txt).


## Performance

### Recommendations (link prediction)
| Model | Dataset | Valid RMSE | Test RMSE | \#Parameters  |
|:-|:-|:-|:-|:-|
| IGMC | MovieLens | 52.67 | 52.73 | 49k |

### Node classification
| Model | Dataset | Valid Accuracy (%) | Test Accuracy (%) | \#Parameters  |
|:-|:-|:-|:-|:-|
| HGT | Cora | 92.3 | - | 19M |

### Link prediction
| Model | Dataset | Valid AP / AUROC | Test AP / AUROC | \#Parameters  |
|:-|:-|:-|:-|:-|
| HGT | Cora | 92.3 | - | 19M |

## References
[1] M. Zhang and Y. Chen: [Inductive Matrix Completion Based On Graph Neural Networks](https://arxiv.org/abs/1904.12058)

[2] M. Zhang and Y. Chen: [Link Prediction Based on Graph Neural Networks](https://arxiv.org/abs/1802.09691)

[3] Z. Hu *et al.*: [Heterogeneous Graph Transformer](https://arxiv.org/abs/2003.01332)

<!-- [] M. Zhang and Y. Chen: [Labeling Trick: A Theory of Using Graph Neural Networks for Multi-Node Representation Learning](https://arxiv.org/pdf/2010.16103.pdf) -->