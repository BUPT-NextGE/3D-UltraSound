# Standard Plane Localisation in 3D Ultrasound

This software implements a Convolutional Neural Network (CNN) for the automatic localisation of standard scan planes in 3D ultrasound of the fetal head.

Tensorflow implementation of the MICCAI 2018 paper [Standard Plane Detection in 3D Fetal Ultrasound Using an Iterative Transformation Network](https://arxiv.org/abs/1806.07486).
<br/><br/>

![pipeline](pipeline.png)


## Prerequisites

- Python 2.7
- [Tensorflow 1.8.0](https://github.com/tensorflow/tensorflow/tree/r1.8)
- [SciPy](http://www.scipy.org/install.html)
- (Optional) [NiBabel](http://nipy.org/nibabel/installation.html#installation) (for reading NIfTI input)
- (Optional) [Matplotlib](https://matplotlib.org/users/installing.html) (for visualization)
- (Optional) [scikit-image](https://scikit-image.org/download) (for computing SSIM)
- (Optional) [srmg](https://github.com/bishesh/statsCompare-RiemannianManifold-Groups) (for computing Riemannian mean. Already included in this repo)
- (Optional) [transformations.py](https://www.lfd.uci.edu/~gohlke/code/transformations.py.html) (for computations on rotation matrices, Euler angles and quaternions. Already included in this repo)


## Usage

To train a CNN model:

    $ python train.py
    
To test with an existing CNN model:

    $ python infer.py


## Data

We are not able to share the dataset we used for the paper due to sensitive patient information. However, we have provided a dummy data which is a random noise matrix to mimic the actual data we used.
    

## Results

Ground truth (red) and predicted (green) transcerebellar standard plane

<img src="results_sample/plane_visual/test/data2.png" alt="result1" width="560"/> <img src="results_sample/image_visual/test/data2.png" alt="result2" width="560"/> 

Path taken by the plane over 10 iterations during inference

<img src="results_sample/plane_movie/test/data2.gif" alt="result3" width="570"/> <img src="results_sample/image_movie/test/data2.gif" alt="result4" width="570"/> 


## Author

Yuanwei Li / yuanwei_li@hotmail.com
