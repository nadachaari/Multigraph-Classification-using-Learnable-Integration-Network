# Multigraph-Classification-using-Learnable-Integration-Network

> [Nada Chaari](https://github.com/https://github.com/nadachaari/Multigraph-Classification-using-Learnable-Integration-Network/)<sup>1,2</sup>, [Mohamed Amine Gharsallaoui]<sup>1,3</sup>, [Hatice Camgöz Akdağ]<sup>2</sup>, [Islem Rekik](https://basira-lab.com/)<sup>1</sup>
> <sup>1</sup>BASIRA Lab, Faculty of Computer and Informatics, Istanbul Technical University, Istanbul, Turkey
> <sup>2</sup>Faculty of Management Engineering, Istanbul Technical University, Istanbul, Turkey
> <sup>3</sup>Ecole Polytechnique de Tunisie (EPT), Tunis, Tunisia

> **Abstract:** *Multigraphs with heterogeneous views present one of the most challenging obstacles to classification tasks due to their complexity. Several works based on feature selection have been recently proposed to disentangle the problem of multigraph heterogeneity. However, such techniques have major drawbacks. First , the bulk of such works lies in the vectorization and the flattening operations, failing to preserve and exploit the rich topological properties of the multigraph. Second , they learn the classification process in a dichotomized manner where the cascaded learning steps are pieced in together independently. Hence, such architectures are inherently agnostic to the cumulative estimation error from step to step. To overcome these drawbacks, we introduce MICNet (multigraph integration and classifier network), the first end-to-end graph neural network based model for multigraph classification. First, we learn a single-view graph representation of a heterogeneous multigraph using a GNN based integration model. The integration process in our model helps tease apart the heterogeneity across the different views of the multigraph by generating a subject-specific graph template while pre- serving its geometrical and topological properties. Second, we classify each integrated template using a geometric deep learning block which enables
us to grasp the salient graph features. We train, in end-to-end fashion, these two blocks using a single objective function to optimize the classification performance. We evaluate our MICNet in gender classification using brain multigraphs derived from different cortical measures. We demonstrate that our MICNet significantly outperformed its variants thereby showing its great potential in multigraph classification.*


# Detailed proposed framework pipeline

This work has been published in the Journal of Neural Networks, 2022. Our framework, named multigraph integration
and classi er networks (MICNet), is the first graph neural network model that integrates and classifies multigraphs in an end-to-end fashion based on geometric deep learning architecture. Our learning-based framework comprises two key steps. (1) Learning to optimally construct single-view graphs
from the original heterogeneous multigraphs (Integration block), (2) Embedding the nodes across the layers using consecutive GNN-based architecture to predict the target (classification block). Experimental results against comparison methods demonstrate that our framework can achieve the best results in terms of classification accuracy. We evaluated our proposed framework from brain genomics superstruct project datasets (https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/25833).

More details can be found at: (link to the paper) (https://www.researchgate.net/publication/359539534_Multigraph_Classification_using_Learnable_Integration_Network_with_Application_to_Gender_Fingerprinting).


, . Our framework consists of two main
blocks. We design a multigraph integration block which is inspired from (Yun
et al., 2019) to perform subject-level multigraph integration. This block ensures
the fusion of the heterogeneous views within the same multigraph.
Then, we inject the subject-level integrated graphs into a graph classi cation
block based on several node embedding and pooling layers (Ying et al.,
2018). This block performs sequential hierarchical node embeddings resulting
in simpler graph representations as the network deepens to eventually output
a class score.
