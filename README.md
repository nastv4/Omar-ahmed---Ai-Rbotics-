# Omar-ahmed---Ai-Rbotics-
install ubuntu then ros , install ros2 on jetson nano 
at first, I did install VMware Workstation Player. 
VMware Workstation Player (formerly known as Player Pro) is a free desktop application from VMware.so I can use Linux with ubuntu.
I did have some problems with ubuntu 24.04, ros does not work with ubuntu 24.04 it only works with ubuntu 20.04.
then i did install ubuntu 20.04 so i could install ros probably. 
at the end, ros2 did work with this configuration :

locale  # check for UTF-8
sudo apt update && sudo apt install locales
sudo locale-gen en_US en_US.UTF-8
sudo update-locale LC_ALL=en_US.UTF-8 LANG=en_US.UTF-8
export LANG=en_US.UTF-8
locale  # verify settings
apt-cache policy | grep universe
500 http://us.archive.ubuntu.com/ubuntu focal/universe amd64 Packages
    release v=20.04,o=Ubuntu,a=focal,n=focal,l=Ubuntu,c=universe,b=amd64
sudo apt install software-properties-common
sudo add-apt-repository universe
sudo apt update && sudo apt install curl gnupg2 lsb-release
sudo curl -sSL https://raw.githubusercontent.com/ros/rosdistro/master/ros.key  -o /usr/share/keyrings/ros-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/ros-archive-keyring.gpg] http://packages.ros.org/ros2/ubuntu $(source /etc/os-release && echo $UBUNTU_CODENAME) main" | sudo tee /etc/apt/sources.list.d/ros2.list > /dev/null
sudo apt update
sudo apt upgrade
sudo apt install ros-foxy-desktop
source /opt/ros/foxy/setup.bash





<img width="957" alt="ros2" src="https://user-images.githubusercontent.com/108282195/179371730-6b6b36ef-fb85-4054-9329-d448397858c8.PNG">
