﻿# Indoor Navigation via Vision-Inertial Data Fusion

This is the code associated with paper [First-person indoor navigation via vision-inertial data fusion](https://ieeexplore.ieee.org/abstract/document/8373507)

![Algorithm Result](figs/hallway_results.png =250x)


## Contents   
* [1. Requirement](#1-requirement)
* [2. iPhone App for Collecting Video-IMU](#2-iphone-app-for-collecting-video-imu)
* [3. Running Code for Hallway Video](#3-running-code-for-hallway-video)
* [Citation](#citation)
* [License](#license)

## 1. Requirement 

This code is written with MATLAB R2016b

## 2. iPhone App for Collecting Video-IMU

Contact [Sarah Ostadabbas](ostadabbas@ece.neu.edu) to request access to our iPhone App for collecting synchronous video and IMU data with adjustable frequency   

## 2. Sample Video 

The original video of the hallway used for experiments in the paper along with its IMU measurements collected with our iPhone App is included in `./sample_video/` directory.  

## 3. Running Code for Hallway Video  

Run `demo_vpdetect_modular.m`

This code contains the following sections:

* Read entire video
* Read IMU data
* Synchonize IMU and video (if not)
* Apply GMM Method on each frame
* Straight line grouping
* Find alpha, beta and gamma for each frame from vanishing directions
* Kalman filter fusion of IMU and video
* Horizon line detection
* Plane detection & depth/width inference
* Step counting & finding step locations
* 2D-map generation

## Citation 
If you find our work useful in your research please consider citing our paper:
```
@inproceedings{farnoosh2018first,
  title={First-person indoor navigation via vision-inertial data fusion},
  author={Farnoosh, Amirreza and Nabian, Mohsen and Closas, Pau and Ostadabbas, Sarah},
  booktitle={Position, Location and Navigation Symposium (PLANS), 2018 IEEE/ION},
  pages={1213--1222},
  year={2018},
  organization={IEEE}
}
```
