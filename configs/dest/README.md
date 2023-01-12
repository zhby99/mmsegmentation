# DEST

[DEST: Depth Estimation with Simplified Transformer](https://arxiv.org/abs/2204.13791)

## Introduction

<!-- [ALGORITHM] -->

<a href="https://github.com/NVIDIA/DL4AGX/tree/master/DEST">Official Repo</a>

## Abstract

<!-- [ABSTRACT] -->

Transformer and its variants have shown state-of-the-art results in many vision tasks recently, ranging from image classification to dense prediction. Despite of their success, limited work has been reported on improving the model efficiency for deployment in latency-critical applications, such as autonomous driving and robotic navigation. In this paper, we aim at improving upon the existing transformers in vision, and propose a method for Dense Estimation with Simplified Transformer (DEST), which is efficient and particularly suitable for deployment on GPU-based platforms. Through strategic design choices, our model leads to significant reduction in model size, complexity, as well as inference latency, while achieving superior accuracy as compared to state-of-the-art in the task of self-supervised monocular depth estimation. We also show that our design generalize well to other dense prediction task such as semantic segmentation without bells and whistles.

<!-- [IMAGE] -->

<div align=center>
<img src="./simplifiedAtt.png" width="70%"/>
</div>

## Citation

```bibtex
@article{YangDEST,
  title={Depth Estimation with Simplified Transformer},
  author={Yang, John and An, Le and Dixit, Anurag and Koo, Jinkyu and Park, Su Inn},
  journal={arXiv preprint arXiv:2204.13791},
  year={2022}
}
```

## Results and models

### Cityscapes


| Method    | Backbone | Crop Size | Lr schd | Mem (GB) | Inf time (fps) |  mIoU | mIoU(ms+flip) | config                                                                                                                                 | download                                                                                                                                                                                                                                                                                                                                                                                       |
| --------- | -------- | --------- | ------: | -------: | -------------- | ----: | ------------- | -------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| DEST | SMIT-B0   | 1024x1024 |  160000 |     - | -           | 64.34 | -         | [config](https://github.com/open-mmlab/mmsegmentation/blob/master/configs/dest/dest_simpatt-b0_1024x1024_160k_cityscapes.py) | - | - |
| DEST | SMIT-B1   | 1024x1024 |  160000 |     - | -            | 68.21 | -        | [config](https://github.com/open-mmlab/mmsegmentation/blob/master/configs/dest/dest_simpatt-b1_1024x1024_160k_cityscapes.py) | - | - |
| DEST | SMIT-B2   | 1024x1024 |  160000 |     - | -           | 71.89 | -         | [config](https://github.com/open-mmlab/mmsegmentation/blob/master/configs/dest/dest_simpatt-b2_1024x1024_160k_cityscapes.py) | - | - |
| DEST | SMIT-B3   | 1024x1024 |  160000 |    - | -           | 73.51 | -         | [config](https://github.com/open-mmlab/mmsegmentation/blob/master/configs/dest/dest_simpatt-b3_1024x1024_160k_cityscapes.py) | - | - |
| DEST | SMIT-B4   | 1024x1024 |  160000 |    - | -           | 73.99 | -         | [config](https://github.com/open-mmlab/mmsegmentation/blob/master/configs/dest/dest_simpatt-b4_1024x1024_160k_cityscapes.py) | - | - |
| DEST | SMIT-B5   | 1024x1024 |  160000 |    - | -          | 75.28 | -        | [config](https://github.com/open-mmlab/mmsegmentation/blob/master/configs/dest/dest_simpatt-b5_1024x1024_160k_cityscapes.py) | - | - |


Note:
- The above models are all training from scratch without pretrained backbones. Accuracy can be further enhanced by appropriate pretraining.
- Training of DEST is not very stable, which is sensitive to random seeds.
