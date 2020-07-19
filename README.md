# ROS

## Ubuntu 18.04.4 LTS (Bionic Beaver) NVIDIA Install & Setting

**Dual Boot Ubuntu** -> **"e" key** -> **end of the line "linux" add** <code>nouveau.modeset=0</code> -> **F10**
**Software & Update** -> **Additional Drivers** -> **using NVIDIA driver metapackage from nvidia-driver-440(open source)**

## ROS Melodic Morenia Install

<code>sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'</code>

<code>sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654</code>

<code>sudo apt update</code>

<code>sudo apt install ros-melodic-desktop-full</code>

<pre><code>sudo apt-get install python-pip
sudo pip install -U rosdep</code></pre>

<pre><code>echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc
source ~/.bashrc</code></pre>

<code>sudo apt-get install python-rosinstall python-rosinstall-generator python-wstool build-essential</code>

<code>sudo apt install python-rosdep</code>
### rosdep update
<pre><code>sudo rosdep init
rosdep update</code></pre>
### catkin workspace
<pre><code>mkdir -p catkin_ws/src
cd catkin_ws/
catkin_make</code></pre>
### bash alias 
<pre><code>gedit ~/.bashrc

alias eb =‘gedit ~/.bashrc'
alias sb ='source ~/.bashrc'
alias cw ='cd ~/catkin_ws'
alias cs ='cd ~/catkin_ws/src'
alias cm ='cd ~/catkin_ws && catkin_make'
source /opt/ros/kinetic/setup.bash
source ~/catkin_ws/devel/setup.bash
export ROS_MASTER_URI=http://localhost:11311
export ROS_HOSTNAME=localhost
</code></pre>
### Test
<code>roscore</code>

<code>rosrun turtlesim turtlesim_node</code>

<code>rosrun turtlesim turtle_teleop_key</code>

<code>rqt_graph </code>

## ROS Git
<pre><code>sudo apt-get install git
sudo apt install git</code></pre>

<code>git config -global user.name[NAME]</code>

<code>git config -global user.mail [ADDRESS]</code>

<code>git clone [URL]</code>


## ROS Serial Communication
<pre><code>sudo update
sudo apt install minicom
sudo minicom -s</code></pre>

sudo apt-get install ros-melodic-joy 
ros-melodic-teleop-twist-joy 
ros-melodic-teleop-twist-keyboard 
ros-melodic-laser-proc 
ros-melodic-rgbd-launch 
ros-melodic-depthimage-to-laserscan 
ros-melodic-rosserial-arduino 
ros-melodic-rosserial-python 
ros-melodic-rosserial-server 
ros-melodic-rosserial-client 
ros-melodic-rosserial-msgs 
ros-melodic-amcl 
ros-melodic-map-server 
ros-melodic-move-base 
ros-melodic-urdf 
ros-melodic-xacro 
ros-melodic-compressed-image-transport 
ros-melodic-rqt-image-view 
ros-melodic-gmapping 
ros-melodic-navigation 
ros-melodic-interactive-markers



# Reference
http://wiki.ros.org/ROS
