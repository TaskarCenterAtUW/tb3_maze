[Maze Explorer]


Robots use laser data to explore this maze. 

The turtlebot3 robot will always follow the wall on the left.

If the robot moves too fast / slow, it can change the value
command.angular.z and command.linear.x

--------------------------------------------------------

Before you can run, you need to copy and make the python file 'executable':
1. Open a terminal, type:
    $ cd ~/catkin_ws/src/tb3_maze/script
    
2. In the same terminal, make executable:
    $ chmod + x maze_explorer.py

3. Remember to select the turtlebot3 model:
    $ export TURTLEBOT3_MODEL=burger
--------------------------------------------------------

To run on real robot:

Terminal 1:
$ roscore

Terminal 2: (turn on robot node)
$ ssh pi@raspberrypi.local sudo date -s$(date -Ins)
$ ssh pi@raspberrypi.local
$ roslaunch turtlebot3_bringup turtlebot3_robot.launch

Terminal 3: (turn on laptop remote control node)
$ roslaunch turtlebot3_bringup turtlebot3_remote.launch

Terminal 4: (turn on maze explorer node)
$ rosrun fira_maze maze_explorer.py

--------------------------------------------------------

To run on simulation:

Terminal 1:
$ roscore

Terminal 2: (turn on Gazebo)
$ roslaunch tb3_maze maze_world.launch

Terminal 3: (turn on maze explorer node)
$ rosrun tb3_maze maze_explorer.py

--------------------------------------------------------





