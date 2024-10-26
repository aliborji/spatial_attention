Addressing a fundamental limitation in deep vision models: lack of spatial attention
=====================
July 1, 2024


Manuscript is avaiable at [https://arxiv.org/pdf/2407.01782v1](https://arxiv.org/pdf/2407.01782v1).
-----------


The Proposed Model: 

![model](https://github.com/aliborji/spatial_attention/blob/main/model.png) 



cnn1.py --> a model that uses F.conv2d 

cnn2.py --> a model that uses sequential conv2d by looping over the image

cnn3.py --> a model that uses sequential conv2d by looping over the image and skipping the location where the has not been a change

First run cnn1.py to train a model (uncomment some lines). Then you can run three CNNs and compare the run time. 
Please study the code to understand how the change is implemented. For example, in cnn3, first conv layer is initialized 
with its previous output and only locations with change in the image are updated. This layer then knows which locations it has updated 
and from that generates a change map to send to the fist pooling layer and so on and on ...


-----------

The DemoSegmenter.ipynb notebook illustrated the main concept behind the second proposed solution based on semantic segmentation.

-----------


```
@misc{borji2024attention,
    title={Addressing a fundamental limitation in deep vision
models: lack of spatial attention},
    author={Ali Borji},
    year={2024},
    eprint={2407.01782},
    archivePrefix={arXiv},
    primaryClass={cs.CV}
}
```
