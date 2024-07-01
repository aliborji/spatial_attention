Addressing a fundamental limitation in deep vision models: lack spatial attention
=====================
July 1, 2024

Minimal code to illustrate the lack of spatial attention in CNNs


Manuscript is avaiable in [Arxiv](https://arxiv.xx).



cnn1.py --> a model that uses F.conv2d 

cnn2.py --> a model that uses sequential conv2d by looping over the image

cnn3.py --> a model that uses sequential conv2d by looping over the image and skipping the location where the has not been a change

First run cnn1.py to train a model (uncomment some lines). Then you can run three CNNs and compare the run time. 
Please study the code to understand how the change is implemented. For example, in cnn3, first conv layer is initialized 
with its previous output and only locations with change in the image are updated. This layer then knows which locations it has updated 
and from that generates a change map to send to the fist pooling layer and so on and on ...

```
@misc{borji2020objectnet,
    title={ObjectNet Dataset: Reanalysis and Correction},
    author={Ali Borji},
    year={2020},
    eprint={2004.02042},
    archivePrefix={arXiv},
    primaryClass={cs.CV}
}
```
