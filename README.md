## 1. 准备

- PCL    >= 1.8（工控机已安装）

- Eigen  >= 3.3.4

- ceres-solver 2.0

- **livox_ros_driver**  [下载地址](https://github.com/Livox-SDK/livox_ros_driver)

  

## 2. 下载和编译

```
cd ~/catkin_ws/src
git clone https://github.com/hku-mars/LiDAR_IMU_Init.git
cd ..
catkin_make -j
source devel/setup.bash
```



## 3. 运行

3.1 在运行前先确定

- 使用的雷达型号(在config文件夹中包含了一些常用的雷达型号)
- config文件夹中的yaml文件中定义了相应的话题名和参数。`lid_topic`和`imu_topic`分别定义了该程序中使用的话题名，必须与自己的雷达和IMU发布的话题名一致。


设置好参数和话题名后，开始运行程序

```
cd catkin_ws
source devel/setup.bash
roslaunch lidar_imu_init xxx.launch
```

程序运行完成后，运行结果存储的路径在

catkin_ws/src/LiDAR_IMU_Init/result/Initialization_result.txt

### 4. 最后

更多细节参看->[README.bak.md](./README.bak.md)
