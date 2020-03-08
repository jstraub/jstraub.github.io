---
title: "Reconstructing Scenes with Mirror and Glass Surfaces"
header:
  teaser: mirrorAndGlass.png
conference: SIGGRAPH
links: 
 - paper: 
   link: /download/whelan2018mirrorAndGlass.pdf
   name: "Paper"
 - bibtex: 
   name: "Bibtex"
 - video: 
   link: https://research.fb.com/publications/reconstructing-scenes-with-mirror-and-glass-surfaces/ 
   name: "Video"
---

Planar reflective surfaces such as glass and mirrors are notoriously hard to reconstruct for most current 3D scanning techniques. When treated naïvely, they introduce duplicate scene structures, effectively destroying the reconstruction altogether. Our key insight is that an easy to identify structure attached to the scanner - in our case an AprilTag - can yield reliable information about the existence and the geometry of glass and mirror surfaces in a scene. We introduce a fully automatic pipeline that allows us to reconstruct the geometry and extent of planar glass and mirror surfaces while being able to distinguish between the two. Furthermore, our system can automatically segment observations of multiple reflective surfaces in a scene based on their estimated planes and locations. In the proposed setup, minimal additional hardware is needed to create high-quality results. We demonstrate this using reconstructions of several scenes with a variety of real mirrors and glass.

{% include base_path %}

## Bibtex <a id="bibtex"></a>
```
@article{whelan2018reconstructing,
  title={Reconstructing scenes with mirror and glass surfaces},
  author={Whelan, Thomas and Goesele, Michael and Lovegrove, Steven J and Straub, Julian and Green, Simon and Szeliski, Richard and Butterfield, Steven and Verma, Shobhit and Newcombe, Richard},
  journal={ACM Transactions on Graphics (TOG)},
  volume={37},
  number={4},
  pages={102},
  year={2018},
  publisher={ACM}
}
```


