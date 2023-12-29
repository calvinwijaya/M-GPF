# M-GPF
This repo contain personal modification of Ground Plane Fit algorithm proposed in the work of [Zermas et al. (2017)](https://ieeexplore.ieee.org/abstract/document/7989591). Check the original paper at [IEEE Xplore](https://ieeexplore.ieee.org/abstract/document/7989591). The modification only add PCD format as option for input data also user now can specify path for data input. For complete use and explanation, please check the [original repo](https://github.com/chrise96/3D_Ground_Segmentation).

## Prerequisites
Install LAStools:
```
wget  http://lastools.github.io/download/LAStools.zip
unzip LAStools.zip
cd LAStools; mv LASlib/src/LASlib-config.cmake LASlib/src/laslib-config.cmake
mkdir build; cd build
cmake ..
sudo make install
```
Install PCL:
```
sudo apt install libpcl-dev
```

## Instalations
Download
```
git clone https://github.com/Amsterdam-AI-Team/3D_Ground_Segmentation.git
```
Build
```
mkdir build  
cd build
cmake ..
make
```

## How to use
```
cd build
./ground_plane_fit ./data/input1.pcd
```

# Citation
Original paper:
```
@INPROCEEDINGS{7989591,
  author={Zermas, Dimitris and Izzat, Izzat and Papanikolopoulos, Nikolaos},
  booktitle={2017 IEEE International Conference on Robotics and Automation (ICRA)}, 
  title={Fast segmentation of 3D point clouds: A paradigm on LiDAR data for autonomous vehicle applications}, 
  year={2017},
  volume={},
  number={},
  pages={5067-5073},
  doi={10.1109/ICRA.2017.7989591}}
```
Original repo: 
> https://github.com/chrise96/3D_Ground_Segmentation
