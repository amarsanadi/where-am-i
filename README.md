# Prject: where-am-i

Localisation of a robot using the ROS AMCL package inside a static map in the Gazebo environment. 

Use teleop mode or a navigation goal via RViz to move the robot within the environment and watch the robot localise itself within the map. 

The ScreenShots folder has screenshots of RViz and Gazebo right after launch and a few more screenshots of the Robot after it has navigated to 3 navigation goals. 

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for testing purposes.

### Prerequisites


```
$ sudo apt-get install ros-kinetic-navigation
$ sudo apt-get install ros-kinetic-map-server
$ sudo apt-get install ros-kinetic-move-base
$ sudo apt-get install ros-kinetic-amcl

```

### Installing

Create a folder in your workspace. 
Clone the repository into a src directory and run catkin_make

```
$ mkdir test_where_am_i

$ cd test_where_am_i

$ git clone https://github.com/amarsanadi/where-am-i.git src

$ catkin_make
```

Open a terminal window.
Launch the world with the robot in it. 


```
source devel/setup.bash
roslaunch my_robot world.launch
```

Open another terminal window and launch amcl. 

```
source devel/setup.bash
roslaunch my_robot world.launch
```

Set a nav goal in RViz. The robot will localise itself and navigate to the goal. 
