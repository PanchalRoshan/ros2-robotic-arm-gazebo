# 🤖 ROS 2 Robotic Arm Simulation with Gazebo

A ROS 2 robotic arm simulation project developed using **URDF/Xacro, RViz, Gazebo Sim, joint control, and ROS–Gazebo communication**.

The project includes a custom robot description, visualization in RViz, and a Gazebo simulation environment containing a warehouse-style scene.

## 📸 Project Preview

### Gazebo Simulation

### RViz Visualization

---

## 🚀 Features

* 🤖 Custom robotic arm/robot model using **URDF and Xacro**
* 📐 Modular robot description using Xacro files
* 🌐 Gazebo Sim environment for robot simulation
* 🖥️ RViz visualization
* ⚙️ Joint configuration and control
* 🔄 Robot state publishing using `robot_state_publisher`
* 🔗 ROS 2 ↔ Gazebo communication using `ros_gz_bridge`
* 🌍 Custom Gazebo world
* 🎛️ Configurable robot parameters
* 📦 Modular ROS 2 package structure

---

## 🛠️ Technologies Used

| Technology              | Purpose                               |
| ----------------------- | ------------------------------------- |
| ROS 2                   | Robot middleware and communication    |
| URDF                    | Robot model description               |
| Xacro                   | Modular robot description             |
| Gazebo Sim              | Physics-based simulation              |
| RViz2                   | Robot visualization                   |
| `robot_state_publisher` | Publishes robot link/joint transforms |
| `ros_gz_bridge`         | ROS 2 ↔ Gazebo communication          |
| CMake                   | Package build system                  |
| Ubuntu                  | Development environment               |

---

## 📁 Project Structure

```text
ros2-robotic-arm-gazebo/
│
├── images/
│   ├── gazebo-simulation.png
│   └── rviz-robot.png
│
├── src/
│   │
│   ├── my_robot_description/
│   │   ├── launch/
│   │   ├── rviz/
│   │   ├── urdf/
│   │   ├── CMakeLists.txt
│   │   └── package.xml
│   │
│   └── my_robot_bringup2/
│       ├── config/
│       ├── launch/
│       ├── worlds/
│       ├── CMakeLists.txt
│       └── package.xml
│
├── .gitignore
└── README.md
```

---

## 🧩 ROS 2 Packages

### `my_robot_description`

Contains the robot model and visualization files.

Main components:

* URDF/Xacro robot description
* Robot links and joints
* Gazebo-specific Xacro configuration
* RViz configuration
* Robot visualization launch files

### `my_robot_bringup2`

Contains the simulation and bringup configuration.

Main components:

* Gazebo launch files
* Gazebo world files
* Simulation configuration
* ROS 2–Gazebo bridge configuration
* Robot spawning and simulation setup

---

## 🖥️ RViz Visualization

To visualize the robot model in RViz:

```bash
ros2 launch my_robot_description display.launch.xml
```

This launches the robot description and RViz visualization.

---

## 🌍 Gazebo Simulation

To launch the complete simulation:

```bash
ros2 launch my_robot_bringup2 my_robot_gazebo.xml
```

This starts the Gazebo simulation with the custom world and robot.

The simulation includes a warehouse-style environment with shelves, boxes, furniture, and the robot.

---

## 🔗 ROS 2 and Gazebo Integration

The project uses `ros_gz_bridge` to establish communication between ROS 2 and Gazebo.

The bridge allows selected Gazebo topics to communicate with ROS 2 topics, enabling ROS 2 nodes and tools to interact with the simulated robot.

The project also uses:

```text
robot_state_publisher
```

to publish the robot's link and joint transformations based on the robot description.

---

## 🦾 Robot Description

The robot is defined using modular Xacro files.

The description package contains components such as:

```text
urdf/
├── arm.xacro
├── arm_gazebo.xacro
├── camera.xacro
├── common_properties.xacro
├── mobile_base.xacro
├── mobile_base_gazebo.xacro
├── my_robot.urdf.xacro
└── standalone_arm.urdf.xacro
```

Using Xacro makes the robot description easier to maintain by allowing reusable properties, macros, and modular components.

---

## ⚙️ Build the Workspace

Create or use a ROS 2 workspace and place the packages inside the `src` directory.

From the workspace root:

```bash
cd ~/ros2_ws
```

Build the packages:

```bash
colcon build
```

Source the workspace:

```bash
source install/setup.bash
```

---

## ▶️ Run the Project

### 1. Source ROS 2

```bash
source /opt/ros/jazzy/setup.bash
```

### 2. Source the workspace

```bash
source ~/ros2_ws/install/setup.bash
```

### 3. Launch RViz

```bash
ros2 launch my_robot_description display.launch.xml
```

### 4. Launch Gazebo

```bash
ros2 launch my_robot_bringup2 my_robot_gazebo.xml
```

---

## 📚 What I Learned

Through this project, I gained practical experience with:

* ROS 2 package development
* URDF and Xacro
* Robot links and joints
* Robot state publishing
* RViz2 visualization
* Gazebo simulation
* Gazebo worlds
* ROS 2 topics
* ROS 2–Gazebo bridging
* Launch files
* Simulation configuration
* Debugging ROS 2 and Gazebo communication

---

## 🔮 Future Improvements

Possible future improvements include:

* 🎮 Improved robotic arm teleoperation
* 🧭 Motion planning with MoveIt 2
* 📍 End-effector position control
* 🤖 Autonomous pick-and-place operations
* 📷 Camera-based object detection
* 📦 Object manipulation in Gazebo
* 🎯 Inverse kinematics
* 🧠 Integration with higher-level autonomous behaviors

---

## 👨‍💻 Author

**Roshan Panchal**

ROS 2 | Robotics | Python | C++ | Gazebo | QA Automation

---

## ⭐ Project

If you find this project useful or interesting, consider giving the repository a ⭐.
