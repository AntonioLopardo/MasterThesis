# MasterThesis

## Abstract

Vector databases are designed to store unstructured data in semantically mean-
ingful representations. Approximate nearest neighbor search (ANNS) is the pri-
mary query method for vector DBs, and the inverted file index (IVF) is among
the most popular ANNS techniques. IVF indexes use clustering to dynamically
reduce the search space based on the query. A high-quality IVF index minimizes
the number of vectors that need to be scanned to reach high recall. The objec-
tive we set out to achieve with this thesis was to understand and characterize the
effectiveness of different techniques and training procedures used to build perfor-
mant IVF indexes that can hold billions of vectors. To achieve this, we compared
a form of hierarchical clustering (HC) recently applied to building these indexes
with more computationally intensive flat clustering (FC) techniques widely im-
plemented in ANNS libraries. We experimented with training with cluster size
penalties, with gradient descent, or using different centroids update frequencies.
We also tested the importance of replication to avoid boundary issues in IVF in-
dexes. Our results show that HC has competitive performance compared to flat
clustering, despite its lower asymptotic complexity, and that it is also beneficial
as an initialization procedure to seed flat clustering. Moreover, HC initialization
speeds up convergence of flat clustering with k-means, and on some datasets, it
improves recall@10 performance at convergence when compared to a clustering
initialized with uniformly sampled points from the dataset. Ultimately, using
the results of our experiments, we created a comprehensive set of recommen-
dations that helps identify the most appropriate techniques to be applied when
building IVF indexes by users with varying computational budgets.
