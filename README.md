andosc_teleop ( ros fuerte )
=============

Use Android andOSC to control robot.

Cheng-Lung Lee, 
University of Detroit Mercy, Advanced Mobile Robotics Lab.


To use it you need rososc 

* Setup rososc
rosws set rososc --git --version=master git://github.com/Auburn-Automow/rososc.git
rosws update rososc

# Install dependency 
sudo apt-get install python-pip libavahi-compat-libdnssd1 python-lxml python-pip
sudo pip install pybonjour txosc

rosmake touchosc_msgs


# Setup andosc_teleop
# Use Android cell phone to control robot , with andOSC (free)

rosws set andosc_teleop --version=master --git https://github.com/udmamrl/andosc_teleop.git

rosmake andosc_teleop

# To run ,In Android phone download andOSC from Google Play for free
Set up andOSC , connect to ROS master IP , port 9000

# run andosc_teleop
roslaunch andosc_teleop andosc_teleop.launch 


