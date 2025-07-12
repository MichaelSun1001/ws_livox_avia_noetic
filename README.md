
# 编译驱动

catkin_make

# 运行可视化的驱动（点云是pointcloud类型）

source devel/setup.sh
roslaunch livox_ros_driver livox_lidar_rviz.launch

# 运行无可视化的驱动（自定义msg）

source devel/setup.sh
roslaunch livox_ros_driver livox_lidar_msg.launch

# 使用新的雷达所需要修改的地方

1. 驱动的launch文件：bd_list
2. livox_lidar_config.json中的broadcast_code、enable_connect
3. 注意如果使用了bd_list可以不用修改config中的参数了
4. 注意在序列号后面加上“1”，因为不同的lidar类型需要加上不同的数字，详情见官方README.md
5. 注意电脑的IP和雷达的IP要在同一个网段，常用：192.168.1.50
