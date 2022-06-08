# A STUDY OF TDA METHODS FOR SCRNA VELOCITY

Reducing and visualizing high dimensional data is a complex challenge, yet is an essential element of
research in computational biology. In this paper, we will examine a particular type of high dimensional
data called RNA velocity, which consists of a point cloud of single cell RNA expression values along with
RNA velocity vectors. Visualizing RNA velocity in low dimensions requires a method to embed both the
point cloud and the velocity vector field.


UMAP is the standard method for embedding the point cloud, and for the vector field, the predominant
algorithm is the ScVelo algorithm. These methods experience two main problems. Firstly, the two
embeddings depend on many arbitrary parameters, where it is difficult to get the best combination
for visualization. Secondly, we have no way to quantify the distortion of the data by the embedding.
Accordingly, this report presents how the RNA velocity embedding works, and make suggestions for its
improvement.


In this paper, we explore the influence of parameters in UMAP and the ScVelo algorithm in both biological
and synthetic datasets. In particular, we provide examples where a small change in parameters can
reverse the vector field embedding. As a comparison, we tested learnable UMAP, a version of UMAP
with learnable parameters, and find that it outperforms UMAP in low-dimension synthetic point cloud
examples.


To quantify the distortion and test the accuracy of our methods, we choose to embed the data back from
low to high dimensions. The ability to reverse the embedding provides a quantification of the loss of
information and will be poor in quality in distorted regions. Further, we use the Jacobian of the inverse
function from learnable UMAP to embed velocities back into high dimensional space.
In the future, we envision that our method could be used to detect highly distorted regions of the vector
field by current embedding methods.


Keywords: RNA velocity, high dimensional data embedding, UMAP, learnable UMAP, ScVelo.


## try of UMAP parameter
  
This jupyter notebook contains some tests of parameters for parametric UMAP (data embedding method) implementation and can be used to generate plot from these tests. 
  
  
## try of ScVelo parameter
  
This jupyter notebook contains some tests of parameters for ScVelo (velocity embedding method) implementation and can be used to generate plot from these tests. 
  
  
## parametrisation
  
This jupyter notebook contains the main part of this project.
It's contains : 

•synthetic dataset generation and biological data

• test for UMAP and parametric UMAP

• new methods for velocity embedding (implementation and test) 

• methods for velocity and dataset inverse embedding

• verification for test of the jacobian and scvelo using PCA
  

JUPYTER NOTEBOOK - PYTHON
