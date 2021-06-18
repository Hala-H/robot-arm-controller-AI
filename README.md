# robot-arm-controller-AI
Smart Methods internship - Task 1 - AI and Robotics track

<h2> Virtualbox and Ubuntu Installation Steps </h2>
<ol>
  <li> Install the most recent Oracel VM virtual box version that suits your system's requirements </li>
  <li> Install Ubuntu 18.04 version as an iso image </li>
  <li> From Vbox click new and add the iso image you just downloaded. </li>
  <li> Follow the steps and wait until Ubuntu works. Be patient, it might take some time! </li>
</ol>

<h2> ROS Installation Steps </h2>
<p> Followed the steps here: <a href=http://wiki.ros.org/melodic/Installation/Ubuntu> http://wiki.ros.org/melodic/Installation/Ubuntu </a> </p>
<ol>
  <li> Choose Ubuntu (or your OS) </li>
  <li> Write the following commands in order: </li>
    <code> sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list' </code> <br>
    <code> curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add - </code> <br>
    <code> sudo apt update </code> <br>
    <code> sudo apt install ros-melodic-desktop-full </code> <br>
    <code> echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc </code> <br>
    <code> source ~/.bashrc </code> <br>
    <code> sudo apt install python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential </code> <br>
    <code> sudo apt install python-rosdep </code> <br>
    <code> sudo rosdep init </code> <br>
    <code> rosdep update </code> <br>
    <code> roscore </code> <br>
  <li> Preparing ROSE (installing catkin workspace) </li> 
    <code> source /opt/ros/noetic/setup.bash </code> <br>
    <code> mkdir -p ~/catkin_ws/src </code> <br>
    <code> cd ~/catkin_ws/ </code> <br>
    <code> catkin_make </code> <br>
    <code> echo "source ~/catkin_ws/devel/setup.bash" >> ~/.bashrc </code> <br>
    <code> source ~/.bashrc </code> <br>
    <code> source devel/setup.bash </code> <br>
    <code> echo $ROS_PACKAGE_PATH </code> <br>
    <code> /home/youruser/catkin_ws/src:/opt/ros/kinetic/share </code> <br>
  <li> Installing the arduino robot arm package from Smart Methods github https://github.com/smart-methods/arduino_robot_arm to the src folder in catkin </li>
    <code> cd ~/catkin_ws/src </code> <br>
    <code> sudo apt install git </code> <br>
    <code> git clone https://github.com/smart-methods/arduino_robot_arm  </code> <br>
  <li> Installing the dependencies </li>
    <code> cd ~/catkin_ws </code> <br>
    <code> rosdep install --from-paths src --ignore-src -r -y </code> <br>
    <code> 	sudo apt-get install ros-melodic-moveit </code> <br>
    <code> 	sudo apt-get install ros-melodic-joint-state-publisher ros-melodic-joint-state-publisher-gui </code> <br>
    <code> 	sudo apt-get install ros-melodic-gazebo-ros-control joint-state-publisher </code> <br>
    <code> 	sudo apt-get install ros-melodic-ros-controllers ros-melodic-ros-control </code> <br>
  <li> Compiling the package </li>
    <code> catkin_make </code> <br>
  <li> Launching Rviz </li>
    <code> roslaunch robot_arm_pkg check_motors.launch </code> <br>
  <li> Gazebo </li>
    <code> roslaunch robot_arm_pkg check_motors.launch </code> <br>
    <code> roslaunch robot_arm_pkg check_motors_gazebo.launch </code> <br>
    <code> rosrun robot_arm_pkg joint_states_to_gazebo.py </code> <br>
  <li> Moveit in Rviz </li>
    <code> roslaunch moveit_pkg demo.launch </code> <br>
  <li> Gazebo and Moveit </li>
    <code> roslaunch moveit_pkg demo_gazebo.launch </code> <br>

</ol>
