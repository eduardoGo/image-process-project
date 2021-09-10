## Project for Digital Image Process | Eduardo G. dos Santos

### Paper: An Effective Loss Function for Generating 3D Models from Single 2D Image without Rendering
#### Reference: [Papers with code](https://paperswithcode.com/paper/an-effective-loss-function-for-generating-3d) | [Paper](https://arxiv.org/abs/2103.03390)

## Dificults

The main dificult was to adapt the code to run on Google Colab, because I have to run with Anaconda package manager with specific version of the some packages and python.

# Paper Context

The current models required a rendering step to apply Single-View 3D Reconstruction. In rendering step is used one very sucess approach called "Differentiable rendering", which is a novel field that allows the gradients of 3D objects to be calculated and propagated through images 2D. The main objective of this paper was to demonstrate that it's possible avoid the rendering step and still get reconstruction results as other state-of-the-art models.

![image](https://user-images.githubusercontent.com/26190178/132851008-24865705-7900-4f58-98c7-df7721d638bb.png)

The image above show the main process. 
- First, the neural network generates a cloud poins from some 2d images  (from different view-angles).
- Second, It is applied a Poisson Surface Reconstruction to generate 3D mesh from given 3D point cloud.
- Finally, the authors use a Generative Adversarial Network (GAN) for texture mapping on a particular 3D mesh and produce a textured 3D mesh based on the input image texture.
