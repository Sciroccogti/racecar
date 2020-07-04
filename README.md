# 智能车仿真
代码使用参考教程：[教程地址](https://www.guyuehome.com/6463)

第三方教程：[Ubuntu18.04下利用Gazebo搭建赛道完成ROS机器人定位导航仿真【智能车】](https://blog.csdn.net/qq_44830040/article/details/107032569)

## Ubuntu18.04 环境配置

ROS 安装请见[官方教程](http://wiki.ros.org/melodic/Installation/Ubuntu)

安装完毕后，安装如下软件包：

```bash
sudo apt install ros-melodic-driver-base ros-melodic-gazebo-ros-control ros-melodic-effort-controllers\
ros-melodic-joint-state-controller ros-melodic-ackermann-msgs ros-melodic-global-planner ros-melodic-teb-local-planner\
ros-melodic-navigation ros-melodic-map-server ros-melodic-gmapping ros-melodic-rtabmap-ros
```

## 报错findline.cpp找不到opencv头文件
执行：`locate OpenCVConfig.cmake`得到你的opencv的路径

执行：`gedit ~/racecar_ws/src/racecar_gazebo/CMakeLists.txt`

修改第7行的路径成你的路径:set(OpenCV_DIR /opt/ros/kinetic/share/OpenCV-3.3.1-dev/)
