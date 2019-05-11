# CoauthorshipRelationshipPrediction

Abstract

The problem of predicting links or interactions between objects in a network, is an important task in network analysis. Along this line, link prediction between co-authors in a co-author network is a frequently studied problem. In most of these studies, authors are considered in a homogeneous network, i.e., only one type of objects (author type) and one type of links(co-authorship) exist in the network. However, in a real bibliographic network, there are multiple types of objects (e.g., venues, topics, papers) and multiple types of links among these objects. In this paper, we study the problem of co-author relationship prediction in the heterogeneous bibliographic network, and a new methodology called Path Predict, i.e., meta path-based relationship prediction model, is proposed to solve this problem. First, meta path-based topological features are systematically extracted from the network. Then, a supervised model is used to learn the best weights associated with different topological features in deciding the co-author relationships. We present experiments on areal bibliographic network, the DBLP network, which show that meta path-based heterogeneous topological features can generate more accurate prediction results as compared to homogeneous topological features. 
In addition, the level of signiﬁcance of each topological feature can be learned from the model, which is helpful in understanding the mechanism behind the relationship building.

Measure Functions on Meta Paths

Once the topologies given by meta paths are determined, the next stage is to propose measures on these meta paths. In this paper, we propose four measures along the lines of topological features in homogeneous networks. These are path count, normalized path count, random walk, and symmetric random walk, which are deﬁned as follows. 
• Path count. 
Path count measures the number of path instances between two objects following a given meta path, denoted as PCR, where R is the relation denoted by the meta path. Path count can be calculated by the products of adjacency matrices associated with each relation in the meta path. 
• Normalized path count. 
Normalized path count is to discount the number of paths between two objects in the network by their overall connectivity, and is deﬁned as NPCR(ai,aj) = PCR(ai,aj)+PCR−1(aj,ai) PCR(ai,·)+PCR(·,aj) , where R−1 denotes the inverse relation of R, PCR(ai,·) denotes the total number of paths following R starting with ai, and PCR(·,aj) denotes the total number of paths following R ending with aj. PCR(ai,·) and PCR(·,aj) can be viewed as degrees of ai and aj in the network respective to R and R−1. 
• Random walk. 
Random walk measure along a meta path is deﬁned as RWR(ai,aj) = PCR(ai,aj) PCR(ai,·) , which is a natural generalization of PropFlow. 
• Symmetric random walk. 
Symmetric random walk considers the random walk from two directions along the meta path, and deﬁned as SRWR(ai,aj) = RWR(ai,aj)+RWR−1(aj,ai).



