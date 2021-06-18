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
    <code> sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list' </code><br>
    <code> curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add - </code>
    <code> sudo apt update </code>
    <code> sudo apt install ros-melodic-desktop-full </code>
    <code> echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc </code>
    <code> source ~/.bashrc </code>
    <code> sudo apt install python-rosdep python-rosinstall python-rosinstall-generator python-wstool build-essential </code>
    <code> sudo apt install python-rosdep </code>
    <code> sudo rosdep init </code>
    <code> rosdep update </code>
    <code> roscore </code>
  <li> Preparing ROSE (installing catkin workspace) </li>
    <code> source /opt/ros/noetic/setup.bash </code>
    <code> mkdir -p ~/catkin_ws/src </code>
    <code> cd ~/catkin_ws/ </code>
    <code> catkin_make </code>
    <code> echo "source ~/catkin_ws/devel/setup.bash" >> ~/.bashrc </code>
    <code> source ~/.bashrc </code>
    <code> source devel/setup.bash </code>
    <code> echo $ROS_PACKAGE_PATH </code>
    <code> /home/youruser/catkin_ws/src:/opt/ros/kinetic/share </code>
</ol>
