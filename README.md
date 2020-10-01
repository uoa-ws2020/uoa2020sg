# uoa2020sg

## Introduction 
This repository provides a set of files for robot simulation models made for the university of Aizu practice session for the tunnel disaster response and recovery challenge in the disaster robotics challenge in World Robot Summit 2020. We are welcome if you are interested in and join to this session. 

Most of the files in this repository come from the repository of WRS-TDRRC-2020SG1
(https://github.com/WRS-TDRRC/WRS-TDRRC-2020SG1). We have modified it slightly for our purpose. 

## SOFTWARE IMPORTANT INFORMATION 
### ABOUT Choreonoid 
Version 1.8 with a tag specified by the development version management. <br>
EX.) git clone -b tag https://github.com/choreonoid/choreonoid.git 

### ABOUT Robotic middle-ware 
 * Recommend using ROS1 Melodic 
We have got information that the choreonoid developer will support the connection between choreonoid and ROS1. 

 * Not recommend using OpenRTM 
We got information that the choreonoid developer does not have any plan to support the connection between choreonoid and RTM. 
There is information that the RTM version 1.1.2 and 1.2.0 were used with older choreonoid. But there is no information on whether the choreonoid developer will support.  
 
### ABOUT AGX Dynamics 
We are considering a suitable version of AGX. 
Currently, the version 2.23.0.4 and higher (the latest 2.29.0.0) are available. 
We recommend the version 2.29.0.0, which is verified by the committee. 

## Requirements
  1. [Choreonoid](https://choreonoid.org/en/manuals/latest/index.html), [Installing Choreonoid](https://choreonoid.org/en/manuals/latest/install/build-ubuntu.html#development-version). If you use ROS melodic, see also [Teleoperation Sample using ROS](https://choreonoid.org/en/manuals/latest/wrs2018/teleoperation-ros.html)  
  2. [AGX for Choreonoid](https://choreonoid.org/en/manuals/latest/agxdynamics/index.html), [Downloading AGX](https://www.algoryx.se/download/?id=1887), [Installing AGX](https://www.algoryx.se/documentation/complete/agx/tags/latest/UserManual/source/installation.html#install-on-ubuntu-16-04). The latest version of AGX is 2.29.0.0 which is verified running under Ubuntu 18.04. 

## How to use this repository 
If you install choreonoid the first time, please follow below commands: 

    $ cd ~  
    $ git clone https://github.com/choreonoid/choreonoid.git  
    $ ~/choreonoid/misc/script/install-requisites-ubuntu-18.04.sh  
    $ sudo apt-get install qt5-default libqt5x11extras5-dev qt5-style-plugins  
    $ cd ~/choreonoid/ext  
    $ git clone https://github.com/uoa-ws2020/uoa2020sg.git 
    $ cd ~/choreonoid && mkdir build && cd build  
    $ cmake .. -DBUILD_AGX_DYNAMICS_PLUGIN=ON -DBUILD_AGX_BODYEXTENSION_PLUGIN=ON -DBUILD_COMPETITION_PLUGIN=ON -DENABLE_CORBA=ON -DBUILD_CORBA_PLUGIN=ON -DBUILD_MULTICOPTER_PLUGIN=ON -DBUILD_MULTICOPTER_SAMPLES=ON -DBUILD_SCENE_EFFECTS_PLUGIN=ON -DBUILD_WRS2018=ON -DUSE_PYTHON3=OFF
    $ make -j4
  
Or you are already using choreonoid, please follow below commands:  
(When your choreonoid is under ~/choreonoid)  

    $ cd ~/choreonoid/ext  
    $ git clone https://github.com/uoa-ws2020/uoa2020sg.git 
    $ cd ~/choreonoid/build  
    $ cmake .. -DBUILD_AGX_DYNAMICS_PLUGIN=ON -DBUILD_AGX_BODYEXTENSION_PLUGIN=ON -DBUILD_COMPETITION_PLUGIN=ON -DENABLE_CORBA=ON -DBUILD_CORBA_PLUGIN=ON -DBUILD_MULTICOPTER_PLUGIN=ON -DBUILD_MULTICOPTER_SAMPLES=ON -DBUILD_SCENE_EFFECTS_PLUGIN=ON -DBUILD_WRS2018=ON -DUSE_PYTHON3=OFF 
    $ make -j4

Before run, you have to add "source /opt/Algoryx/AgX-"Version"/setup_env.bash" at the end of ~/.bashrc , and reopen the terminal.<br>
EX.) "source /opt/Algoryx/AgX-2.29.0.0/setup_env.bash" (when you use version 2.29.0.0)<br>
Please find further details (field images, run scripts, and some attentions related the stage gate rules) in the [wiki page](https://github.com/uoa-ws2020/uoa2020sg/wiki).  

## The location of the simulation log files  
After running a simulation, you can find a simulation log file under ~/choreonoid/ext/uoa2020sg/project.  
Please see also [Choreonoid documentation](https://choreonoid.org/en/manuals/1.7/simulation/execution-and-playback.html).  

## Q&A 
If you have any questions or anything, please feel free contact us. 
Contact Address: uoa-ws2020@u-aizu.ac.jp

## Acknowledgement
We show our great thanks to the organizing committee of the tunnel disaster response and recovery challenge in the disaster robotics challenge in World Robot Summit 2020, because we refer many files to [WRS-TDRRC-2020SG1](https://github.com/WRS-TDRRC/WRS-TDRRC-2020SG1).

Edited: 30th Sep. 2020
