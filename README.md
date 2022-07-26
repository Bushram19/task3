# task3
Installing the arm package.
first step was installing ROS system , now in second step we installing the arm package.
start visit the link I will following the instructions step by step ,, link “https://s-m.com.sa/ros.txt".
I made changing version from kinetic to noetic and change this "source /home/wesam/catkin_ws/devel/setup.bash" to "source /home/BushraM/catkin_ws/devel/setup.bash"

Steps:

mkdir -p ~/catkin_ws/src

cd ~/catkin_ws/

catkin_make

cd ~/catkin_ws/src

git clone https://github.com/smart-methods/arduino_robot_arm.git

cd ~/catkin_ws

rosdep install --from-paths src --ignore-src -r -y

sudo apt-get install ros-noetic-moveit

sudo apt-get install ros-noetic-joint-state-publisher ros-noetic-joint-state-publisher-gui

sudo apt-get install ros-noetic-gazebo-ros-control joint-state-publisher

sudo apt-get install ros-noetic-ros-controllers ros-noetic-ros-control

sudo nano ~/.bashrc

at the end of the (bashrc) file add the follwing line (source /home/BushraM/catkin_ws/devel/setup.bash) then ctrl + o

source ~/.bashrc

roslaunch robot_arm_pkg check_motors.launch

