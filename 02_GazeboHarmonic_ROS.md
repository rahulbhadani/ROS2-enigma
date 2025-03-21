# ROS2 Jazzy with Gazebo Harmonic on Ubuntu 24.04 LTS

After instaling ROS2 Jazzy:
```{bash}
echo "source /opt/ros/humble/setup.bash" >> ~/.bashrc
source ~/.bashrc
```

## Install Gazebo
```{bash}
sudo apt-get install ros-jazzy-ros-gz
```

## Run Gazebo
```{bash}
gz sim
```

# Installing Dependencies
Some common packages 

```{bash}
sudo apt install ros-jazzy-xacro
sudo apt install ros-jazzy-teleop-twist-keyboard
sudo apt install ros-jazzy-joint-state-publisher
sudo apt install ros-jazzy-joint-state-publisher-gui

```
## Creating ROS workspace
```{bash}
mkdir -p ~/ros_ws/src
```
## Build Workspace

```{bash}
cd ~/ros_ws
colcon build
```
If you are gonna use the same workspace, add the following to ~/.bashrc as well.

```{bash}
echo "source ~/ros_ws/install/setup.bash" >> ~/.bashrc
source ~/.bashrc
```

## Creating a Package

```{bash}
cd ~/ros_ws/src
ros2 pkg create --build-type ament_cmake robot_sim
cd  ~/ros_ws/src/robot_sim
mkdir model params launch
```
