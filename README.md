# PolyNet: A Pursuit of Structural Diversity in Very Deep Networks

By [Xingcheng Zhang](https://www.linkedin.com/in/xingchengzhang/), [Zhizhong Li](http://mmlab.ie.cuhk.edu.hk/html_people/postgraduate_Zhizhong_Li.html), [Chen Change Loy](http://personal.ie.cuhk.edu.hk/~ccloy/), [Dahua Lin](http://dahua.me)

[Multimedia Laboratory](http://mmlab.ie.cuhk.edu.hk), The Chinese University of Hong Kong

[![Homepage](https://img.shields.io/badge/Project-Homepage-orange.svg?style=flat&colorA=E1523D&colorB=007D8A)](http://mmlab.ie.cuhk.edu.hk/projects/cu_deeplink/)
[![pdf](https://img.shields.io/badge/Arxiv-pdf-orange.svg?style=flat)](https://arxiv.org/abs/1611.05725)

### BibTeX

```bib
@article{zhang2016polynet,
  title={Polynet: A pursuit of structural diversity in very deep networks},
  author={Zhang, Xingcheng and Li, Zhizhong and Loy, Chen Change and Lin, Dahua},
  journal={arXiv preprint arXiv:1611.05725},
  year={2016}
}
```

### The Very Deep PolyNet
  ![PolyNet](polynet.png)
* [Visualization](http://ethereon.github.io/netscope/#/gist/b22923712859813a051c796b19ce5944)
* Models
    * [Parrots](http://www.parrotsdnn.org): model files to be added;
    * [Caffe](https://github.com/yjxiong/caffe): [proto](https://drive.google.com/open?id=0B6pxsvrUJ931aTJmdEJOODhtQ3c), [model](https://drive.google.com/open?id=0B6pxsvrUJ931WXluclRBVDAtaEk)

  NOTE: the caffe model is converted from the *Parrots* model, and the proto file is based on [Yuanjun's fork](https://github.com/yjxiong/caffe) of Caffe.
  
### Results
model|training speed* (#imgs/second)|single-crop val top-1|single-crop val top-5|single-crop test top-5 | multi-crop val top-1 | multi-crop val top-5
	:---:|:---:|:---:|:---:|:---:|:---:|:---:
  [ResNet-152](https://github.com/KaimingHe/deep-residual-networks) |-| [22.16](https://github.com/facebook/fb.resnet.torch#single-crop-224x224-validation-error-rate) | [6.16](https://github.com/facebook/fb.resnet.torch#single-crop-224x224-validation-error-rate) | - | [19.38](https://arxiv.org/pdf/1512.03385.pdf) | [4.49](https://arxiv.org/pdf/1512.03385.pdf) 
  ResNet-152^ |279 ( 8 GPUs)| 20.93 | 5.54 | 5.50 | 18.50 | 3.97
  ResNet-269^ |245 (16 GPUs)| 19.78 | 4.89 | 4.82 | 17.54 | 3.55
  ResNet-500^ |248 (32 GPUs)| 19.66 | 4.78 | 4.70 | 17.59	| 3.63
  [Inception-v4](https://arxiv.org/abs/1602.07261) |-| 20.0 | 5.0 | -| 1 7.7 | 3.8
  [Inception-ResNet-v2](https://arxiv.org/abs/1602.07261) |-| 19.9 |  4.9 | - | 17.8 | 3.7
  Inception-ResNet-v2 |314 ( 8 GPUs)| 20.05  | 5.05  | 5.11 | 18.41 | 3.98 
  Very Deep Inception-ResNet |278 (32 GPUs)| 19.10 | 4.48 | 4.46 | 17.39  | 3.56
  Very Deep PolyNet |290 (32 GPUs)| **18.71** | **4.25** | **4.33** | **17.36**  | **3.45**

  ^ The ResNet models are trained by [Tong Xiao](https://github.com/Cysu)
 
  \* Training speed is measured on own deep learning framwork [*Parrots*](http://www.parrotsdnn.org).
