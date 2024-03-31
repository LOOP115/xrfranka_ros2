# Franka_Ctrl

<br>

## Instructions

### Dependencies

Please follow this [link](https://github.com/LOOP115/XR_Franka_Hub/blob/main/docs/franka/setup_franka.md) to setup dependencies before using this repository.

### Building

```bash
# Clone the repo and build
git clone https://github.com/LOOP115/franka_ctrl

# Build
cd franka_ctrl
colcon build
```

### Sourcing

Before using this package, remember to source the ROS 2 workspace.

```bash
source install/setup.bash
```

<br>

## Usage

### Examples

```bash
# Move Franka to the default start configuration
ros2 run sim_ctrl move_to_start

# Follow the target inside Ignition Gazebo
ros2 launch ctrl_bringup sim_follow_target.launch.py
```

### ROS Unity Integration

```bash
# Get ROS machine's IP
hostname -I

# Start ROS TCP Server
ros2 run ros_tcp_endpoint default_server_endpoint --ros-args -p ROS_IP:=<IP>

# Follow the target inside Unity
ros2 launch ctrl_bringup sim_follow_unity_target.launch.py
```

