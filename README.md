
# 编译驱动
catkin_make

# 运行可视化的驱动（点云是pointcloud类型）

source devel/setup.sh
roslaunch livox_ros_driver livox_lidar_rviz.launch

# 运行无可视化的驱动（自定义msg）

source devel/setup.sh
roslaunch livox_ros_driver livox_lidar_msg.launch
