# ROS

<hr/>

## Ubuntu 18.04.4 LTS & NVIDIA Install

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

<hr/>

## ROS Git
<pre><code>sudo apt-get install git
sudo apt install git</code></pre>

<code>git config -global user.name[NAME]</code>

<code>git config -global user.mail [ADDRESS]</code>

<code>git clone [URL]</code>

<hr/>

## ROS Serial Communication
<pre><code>sudo update
sudo apt install minicom
sudo minicom -s</code></pre>

<hr/>

# Reference
http://wiki.ros.org/ROS



<pre><code>
sudo apt-get install gcc
sudo apt-get update
sudo apt-get upgrade

sudo rm /etc/apt/sources.list.d/cuda*
sudo apt remove nvidia-cuda-toolkit​
sudo apt purge nvidia-*​
sudo apt update​
​
sudo apt-key adv --fetch-keys  http://developer.download.nvidia.com/\
compute/cuda/repos/ubuntu1804/x86_64/7fa2af80.pub​

sudo bash -c 'echo "deb http://developer.download.nvidia.com/\
compute/cuda/repos/ubuntu1804/x86_64 /" > /etc/apt/sources.list.d/cuda.list'

sudo apt update​
sudo apt install cuda-10-0

nvidia-smi
nvcc -V​

</code></pre>


<pre><code>
# Chrome Install
wget -q -O - https://dl-ssl.google.com/linux/linux_signing_key.pub | sudo apt-key add -
sudo sh -c 'echo "deb [arch=amd64] http://dl.google.com/linux/chrome/deb/ stable main" >> /etc/apt/sources.list.d/google.list'
sudo apt-get update
sudo apt-get install google-chrome-stable
sudo rm -rf /etc/apt/sources.list.d/google.list
sudo apt-get clean

# Synchronize time clock windows-ubuntu
timedatectl set-local-rtc 1
sudo gedit /etc/default/rcS
UTC=no		#in gedit tool

# Change default boot option 
sudo gedit /etc/default/grub
GRUB_DEFAULT=saved	#in gedit tool
sudo update-grub
sudo grub-set-default 2​
grub-editenv list​	#saved_entry=2
</code></pre>

