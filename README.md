andosc_teleop ( ros fuerte )
=============

Use Android andOSC / iOS mrmr OSC controler to control robot.

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

#In Android: To run ,In Android phone download andOSC from Google Play for free
 Set up andOSC , connect to ROS master IP , port 9000
#In iphne/ipad/ipod : download mrmr OSC control
 Setup mrmr OSC
   Server as ROS master IP
   Namespace / 
   port 9000 ,
   Bundle Message Style :On
   Use float Values: On
   Smoothing		: 0.2
   Frequency(ms): 100ms

# run andosc_teleop
roslaunch andosc_teleop andosc_teleop.launch 


