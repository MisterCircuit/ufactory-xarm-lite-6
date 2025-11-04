# uFactory xArm Lite 6 – Assembly & Visualization  
Repository: [https://github.com/MisterCircuit/ufactory-xarm-lite-6](https://github.com/MisterCircuit/ufactory-xarm-lite-6)

This project contains the mechanical build files and ROS/URDF setup for the uFactory xArm Lite 6 robotic arm. It includes visualization support via ROS and RViz so you can clone this repo and view the arm in a simulated environment.

![alt text](image-1.png)


---

## Prerequisites  
Make sure your machine has:

- Ubuntu 22.04 (or a compatible distro)  
- ROS2 installed  
- RViz (part of the ROS installation)  
- ROS URDF Tutorial package (required for launching and visualizing URDF)
 

---
## 1 Install ROS URDF tutorial:
```bash
sudo apt update
```
For ros humble
```bash
sudo apt install ros-humble-urdf-tutorial
```
## 2 Create a workspace for the repository
```bash
mkdir -p ufractor_xarm7_ws/src
cd ufractor_xarm7_ws/src 
```
## 2 Clone the Repository  
```bash
git clone https://github.com/MisterCircuit/ufactory-xarm-lite-6.git  
cd ..  
```
## 3 Build the ROS 2 package
```bash
colcon build --symlink-install
```
## 3 Source your workspace
```bash
source install/setup.bash
```
## 4 Launch Rviz Visualization
```bash
ros2 launch urdf_tutorial display.launch.py model:=$PWD/robot_description/urdf/robott.urdf
```
