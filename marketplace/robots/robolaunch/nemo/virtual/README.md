# <img src="https://raw.githubusercontent.com/robolaunch/trademark/main/logos/svg/rocket.svg" width="40" height="40" align="top"> robolaunch Nemo

## Building Nemo

Install dependencies by running the command below (these packages will be added to ROS 2 dependencies shortly):

```bash
sudo apt-get install -y \
  python3-colcon-common-extensions \
  build-essential \
  g++ \
  python3-dev \
  autotools-dev \
  libicu-dev \
  libbz2-dev \
  libboost-all-dev\
  ros-humble-gazebo-ros2-control \
  ros-humble-ros2-controllers \
  ros-humble-ros2-control \
  ros-humble-diff-drive-controller \
  ros-humble-nav2-* \
  ros-humble-diff-drive-controller \
  ros-humble-joint-state-broadcaster \
  ros-humble-joint-state-publisher \
  ros-humble-slam-toolbox \
  ros-humble-hardware-interface \
  ros-humble-controller-manager \
  ros-humble-xacro \
  ros-humble-twist-mux \
  ros-humble-serial-driver \
  ros-humble-controller-manager \
  ros-humble-gazebo-ros2-control \
  ros-humble-joint-state-broadcaster \
  ros-humble-diff-drive-controller \
  ros-humble-pcl-* \
  ros-humble-joy \
  ros-humble-teleop-twist-joy \
  ros-humble-image-transport-plugins \
  ros-humble-rviz2
```

Build the workspace:

```bash
colcon build
```

## Launching Nemo Nodes

First, start Gazebo:

```bash
ros2 launch articubot_one launch_sim.launch.py
```

Then merge the laser sensor data with the command below:

```bash
ros2 launch ira_laser_tools merge_multi.launch.py
```

Start SLAM Toolbox:

```bash
ros2 launch articubot_one online_async_launch.py
```

Start navigation:

```bash
ros2 launch articubot_one navigation_launch.py
```