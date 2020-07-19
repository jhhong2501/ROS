# ROS

## Ubuntu 18.04.4 LTS (Bionic Beaver) NVIDIA Install

**Dual Boot Ubuntu** -> **"e" key** -> **end of the line "linux" add** <code>nouveau.modeset=0</code> -> **F10**
**Software & Update** -> **Additional Drivers** -> **using NVIDIA driver metapackage from nvidia-driver-440(open source)**

## ROS Melodic Morenia Install

<code>sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'</code>

<code>sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654</code>

<code>sudo apt update</code>

<code>sudo apt install ros-melodic-desktop-full</code>

<code>sudo apt-get install python-pip
sudo pip install -U rosdep</code>

<code>sudo rosdep init
rosdep update</code>

<code>echo "source /opt/ros/melodic/setup.bash" >> ~/.bashrc</code>
source ~/.bashrc

<code>sudo apt-get install python-rosinstall python-rosinstall-generator python-wstool build-essential</code>

<code>mkdir -p catkin_ws/src
cd catkin_ws/
catkin_make</code>


## ROS Serial Communication

<pre><code>sudo update
sudo apt install minicom
sudo minicom -s</code></pre>

