---
title: "StereoDRNet: Dilated Residual Stereo Net"
header:
  teaser: stereodrnet.png
conference: CVPR
links: 
 - paper: 
   link: https://arxiv.org/pdf/1904.02251.pdf
   name: "Paper"
 - bibtex: 
   name: "Bibtex"
 - video: 
   link: https://youtu.be/AkopUYMIxV4 
   name: "Video"
---

We propose a system that uses a convolution neural network (CNN) to estimate depth from a stereo pair followed by volumetric fusion of the predicted depth maps to produce a 3D reconstruction of a scene. Our proposed depth refinement architecture, predicts view-consistent disparity and occlusion maps that helps the fusion system to produce geometrically consistent reconstructions. We utilize 3D dilated convolutions in our proposed cost filtering network that yields better filtering while almost halving the computational cost in comparison to state of the art cost filtering architectures. For feature extraction we use the Vortex Pooling architecture. The proposed method achieves state of the art results in KITTI 2012, KITTI 2015 and ETH 3D stereo benchmarks.  Finally, we demonstrate that our system is able to produce high fidelity 3D scene reconstructions that outperforms the state of the art stereo system.

{% include base_path %}

## Bibtex <a id="bibtex"></a>
```
@article{
  title={StereoDRNet: Dilated Residual Stereo Net},
  author={Chabra, Rohan and Straub, Julian and Sweeny, Chris and Newcombe, Richard and Fuchs, Henry},
  booktitle ={CVPR},
  year={2019}
}
```




