# [Multi-Level Context Ultra-Aggregation for Stereo Matching](https://mmcheng.net/mcua/)

(not completed, please wait a few days.)

## Introduction

Exploiting multi-level context information to cost volume can improve the performance of learning-based stereo matching methods. 
In recent years, 3-D Convolution Neural Networks (3-D CNNs) show the advantages in regularizing cost volume
but are limited by unary features learning in matching cost computation. 
However, existing methods only use features from plain convolution layers or a simple aggregation 
of multi-level features to calculate cost volume, 
which is insufficient because stereo matching requires discriminative features 
to identify corresponding pixels in rectified stereo image pairs. 
In this paper, we propose a unary features descriptor using multi-level context ultra-aggregation (MCUA), 
which encapsulates all convolutional features into a more discriminative representation 
by intra- and inter-level features combination. 
Specifically, a child module that takes low-resolution images as input captures larger context information; 
the larger context information from each layer is densely connected to the main branch of the network. 
MCUA makes good usage of multi-level features with richer context and performs the image-to-image prediction holistically. 
We introduce our MCUA scheme for cost volume calculation and test it on PSM-Net. 
We also evaluate our method on Scene Flow and KITTI 2012/2015 stereo datasets. 
Experimental results show that our method outperforms state-of-the-art methods 
by a notable margin and effectively improves the accuracy of stereo matching.

## Citation

If you are using the code/model/data provided here in a publication, please consider citing our paper:
```
@inproceedings{Nie2019Stereo,
  title={Multi-Level Context Ultra-Aggregation for Stereo Matching},
  author={Guang-Yu Nie and Ming-Ming Cheng and Yun Liu and Zhengfa Liang and Deng-Ping Fan and Yue Liu and Yongtian Wang},
  booktitle={IEEE CVPR},
  year={2019},
}
```

## Usage

### Dependencies

- [Python2.7](https://www.python.org/downloads/)
- [PyTorch(0.4.0+)](http://pytorch.org)
- torchvision 0.2.0 (higher version will cause issues)
- [KITTI Stereo Datasets](http://www.cvlibs.net/datasets/kitti/eval_stereo.php)
- [Scene Flow Datasets](https://lmb.informatik.uni-freiburg.de/resources/datasets/SceneFlowDatasets.en.html)

```
Usage of dataset
Download the datasets, and put them into one folder, named "datasets".

The structure of the folder "datasets" is shown below:

|--datasets
     |--data_scene_flow-kitti2015
          |--testing
          |--training
     |--data_stereo_flow-kitti2012
          |--testing
          |--training
     |--SceneFlowData
          |--disparity
               |--driving
                    |--15mm_focallength
                    |--35mm_focallength
               |--flyingthings3D
                    |--TEST
                         |--A
                         |--B
                         |--C
                    |--TRAIN
                         |--A
                         |--B
                         |--C
               |--monkaa
                    |--a_rain_of_stones_x2
                    |--eating_camera2_x2
                    |--eating_naked_camera2_x2
                    |--...
                    |--treeflight_x2
          |--frames_cleanpass
               |--driving
                    |--15mm_focallength
                    |--35mm_focallength
               |--flyingthings3D
                    |--TEST
                         |--A
                         |--B
                         |--C
                    |--TRAIN
                         |--A
                         |--B
                         |--C
               |--monkaa
                    |--a_rain_of_stones_x2
                    |--eating_camera2_x2
                    |--eating_naked_camera2_x2
                    |--...
                    |--treeflight_x2
```

### Train MCUA

### Validate MCUA

### Train EMCUA

### Validate EMCUA

### Test EMCUA


## Acknowledgment

This code is based on PSM-Net. Thanks to the contributors of PSM-Net.
```
@inproceedings{chang2018pyramid,
  title={Pyramid Stereo Matching Network},
  author={Chang, Jia-Ren and Chen, Yong-Sheng},
  booktitle={Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition},
  pages={5410--5418},
  year={2018}
}
```
