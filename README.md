# iarc7_main
Overall repo for competition-ready code for IARC mission 7. Also holds skeleton of architecture.

## Installation:
### Easy Way:
Install the team VM build of Ubuntu. This has everything you need already installed!
Note: you will need <exact amount> of storage free. 
  * Download VirtualBox if you don't already have some way to run VMs.
  * Install the team VM build of Ubuntu at <link_coming_soon>
 
### Hard Way: 
You already run Ubuntu on your machine, or don't want to use a VM.
Run the following (you can copy and paste the whole thing):
```
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list' && \
sudo apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80 --recv-key 421C365BD9FF1F717815A3895523BAEEB01FA116 && \
sudo apt-get update && \
sudo apt-get install ros-kinetic-desktop-full && \
sudo rosdep init && \
rosdep update
```
Respond `y` to the prompt. This will take about 10+ minutes.

run the following to add ROS environment variables on startup:
```
echo "source /opt/ros/kinetic/setup.bash" >> ~/.bashrc && \
source ~/.bashrc
```
NOTE: If you use zShell, like I do, run the following instead. If you don't know what I'm talking about, ignore this and run the lines above.
```
echo "source /opt/ros/kinetic/setup.zsh" >> ~/.zshrc && \
source ~/.zshrc
```
Make a new ROS workspace:
```
mkdir -p ~/iarc7/src && \
cd ~/iarc7/ && \
catkin_make
```
Source the new setup files (or below for zshell):
```
echo "source ~/iarc7/devel/setup.bash" >> ~/.bashrc && \
source ~/.bashrc;
```
OR for zshell, 
```
echo "source ~/iarc7/devel/setup.zsh" >> ~/.zshrc && \
source ~/.zshrc;
```
Clone (install) our repo!
```
git clone https://github.com/STOC-Machine/iarc7_main.git
```
