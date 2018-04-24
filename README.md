

# TASKONOMY Dataset 

This repository shares a multi-annotated dataset from Taskonomy paper, including ~4 million images from ~600 buildings. Each image has annotations for every one of the 2D, 3D, and semantic tasks in Taskonomy's dictionary (see below). For more details, please see the [CVPR 2018 paper](http://taskonomy.vision/#paper).

Currently we are sharing a small fraction of the dataset as a sample. The full dataset will be released in May 2018. Please contact us if you'd like earlier access.

### See sample results of the TASK BANK trained on the taskonomy here: https://taskonomy.vision/#models
### Try the live demo here: https://taskonomy.vision/tasks
#### Reference Paper: "Taskonomy: Disentangling Task Transfer Learning", CVPR 2018.
Amir R. Zamir, Alexander Sax*, William B. Shen*, Leonidas Guibas, Jitendra Malik, Silvio Savarese. 

http://taskonomy.vision/ 

 
The annotations of a sample image for a subset of 15 tasks:
<div align="center">
  <img src="http://taskonomy.vision/static/images/dataset_thumbnail.png"  width="900px" />
</div>



# sample-model-1
A model, selected at random, from the training set of the paper is shared in the repository. The folder structure is described below:

  
```
curvature/
    Curvature images. 
        Principal curvatures are encoded in the first two channels.
        Zero curvature is encoded as the pixel value 127
depth/
   Z-buffer depth images.
       Units of 1/512m with a max range of 128m.
edge/
    Occlusion (3D) edge images.
edge2d/ 
    2D texture edge images.
keypoint/
    3D keypoint heatmaps.
keypoint2d/
    2D keypoint heatmaps.
modeldata/
    Mesh and metadata about the building.
mist/
    Euclidian distance images.
nonfixated/
    All (point', view') which have line-of-sight and a view of "point" within the camera frustum
normal/
    Surface normal images.
        127-centered
points/
    Metadata about each (point, view).
    For each image, we keep track of the optical center of the image.
    This is uniquely identified by the pair (point, view).
        Contains annotations for:
             Room layout
             Vanishing point
             Point matching
             Relative camera pose esimation (fixated)
             Egomotion
        And other low-dimensional geometry tasks. 
places/
    Scene classification annotations distilled from PlaceNet
rgb/
    RGB images
rgb_large/
    RGB images in 1024x1024 resolution.
reshade/
    Images of the mesh rendered with new lighting.
segmentsemantic/
    Semantic segmentation annotations distilled from [FCIS](https://arxiv.org/pdf/1611.07709.pdf)
segment2d/
   Pixel-level unsupervised superpixel annotations based on RGB.
segment25d/
    Pixel-level unsupervised superpixel annotations based on RGB + Normals + Depth + Curvature.
skybox/
    Skybox images for each camera position in the mesh
softmax1000/
    Object classification (Imagenet 1000) annotation distilled from ResNet-152
```
