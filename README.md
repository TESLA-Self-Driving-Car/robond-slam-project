# robond-slam-project
Robotics Nano-degree Term 2 Project 3: Map My World Robot.

# Setup and Run

## Step by step Execution

Create catkin workspace

```
$ mkdir -p ~/catkin_ws/src
$ cd ~/catkin_ws/src
$ catkin_init_workspace
$ cd ~/catkin_ws
$ catkin_make
```

Copy packages into the catkin workspace:

```
$ cd ~
$ git clone https://github.com/xpharry/robond-slam-project.git
$ cp -r robond-slam-project/rover_bot ~/catkin_ws/src/
```

Copy the content of this repo into slam_project folder, source and build the project:

```
$ cd ~/catkin_ws
$ source devel/setup.bash
$ catkin_make
```

To run the mapping process open up 4 terminals and run following commands seperately:

```
$ cd ~/catkin_ws
$ roslaunch slam_project world.launch world_file:=~/catkin_ws/src/slam_project/worlds/kitchen_dining.world
$ roslaunch slam_project teleop.launch
$ roslaunch slam_project mapping.launch
$ roslaunch slam_project rviz.launch
```

To use the cafe_dining.world instead, run:

```
$ cd ~/catkin_ws
$ roslaunch slam_project world.launch world_file:=~/catkin_ws/src/slam_project/worlds/cafe_dining.world
$ roslaunch slam_project teleop.launch
$ roslaunch slam_project mapping.launch
$ roslaunch slam_project rviz.launch
```

## Single Script Execution

```
cd slam_project/script
./rtab_run
```
