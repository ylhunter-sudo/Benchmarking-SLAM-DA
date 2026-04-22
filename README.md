<p align="center">

  <h1 align="center">Benchmarking of LIDAR/RGB SLAM with Monocular Depth Prior</h1>
  <h3 align="center">
    <strong>Hunter Ylitalo</strong>
    ,
    <strong>Philip Zacharoudis</strong>
    ,
    <strong>Hoang Nguyen</strong>
  </h3>
  <div align="center"></div>
</p>
Assesses multiple forms of SLAM, focused on comparison between [Depth Anything v2](https://github.com/DepthAnything/Depth-Anything-V2) and [v3](https://github.com/ByteDance-Seed/depth-anything-3) as depth estimate for ORB SLAM 3 as a good form of monocular camera-based SLAM and Kiss-ICP as a form of Lidar SLAM.


## Environment Setup 
These scripts were written in [Google Colab](https://colab.research.google.com/) and were run successfully on the T4 GPU runtime environment.
With some updates, they could be used in other environments, but a comparable GPU would be necessary to run Depth Anything.
They are set up to install necessary components.
Individual scripts provide instructions on the required data structure for their use.

## Contents
DAv2-OrbSlam-Hilti.ipynb assesses Depth Anything v2 as a depth estimator for [ORB SLAM 3](https://github.com/UZ-SLAMLab/ORB_SLAM3), and Kiss-ICP on the [Hilti](https://hilti-challenge.com/dataset-2023) dataset and compares the results of each method to Ground Control Points in the dataset for accuracy, scale, and other metrics.

orbslam3_kitti_depth_prior_FULL_weak_keyframes.ipynb is used to run sequences of the [KITTI](https://www.cvlibs.net/datasets/kitti/) dataset through a Depth Anything v3 depth estimator and uses that as the depth input to ORB Slam 3, ORB SLAM 3 on its own, and color/grayscale versions of inputs.  Note: Pangolin installation step may require running on CPU instead of GPU

MBOT_KITTI_Evaluation.ipynb assesses the results of the KITTI dataset in terms of different accuracy metrics.
