Welcome to the WRS-TDRRC-2020SG1 wiki!

# IMPORTANT ATTENTIONS RELATED THE STAGE GATE RULES!  
You should read this section before trying the stage gate.  
1. You have to choose suitable stage gate fields for your robot which you want to assess. Please check the following table to know which stage gate model should be used to assess your robot.  
2. You have to assess your all robots which you will use in the competition. This is meaning that you have to assess a robot again when you modified the robot, for example changing the size of robot, adding or changing arms, legs, wheels, crawlers, and other important things for effecting the real time factor of the simulator.   
3. You have to assess also any additional tools which your robot will use in the competition. This is meaning that you have to assess a tool again when you modified the tool.  

Table: The relations between robots and the stage gate fields(In the table, "V" means suitable combination).  

| Field model name | Large size robot(Ex.:DoubleArmV7) | Middle and small size robot(Ex.:AizuSpider) | Multi-copter(Ex.:Quadcopter) |  
| :-   | :-:  | :-:  | :-:  |
| SG1L |  V   |  -   |  -   |
| SG1M |  -   |  V   |  V   |
| SG2  |  V   |  V   |  -   |

## SG1L  
### Field Image  
![SG1L field overview image](wiki/img/SG1L-WholeView.png)  
Colors may vary.  

### Python Script  
    $ ~/choreonoid/build/bin/choreonoid ~/choreonoid/ext/WRS2020SG/script/SG1L-DoubleArmV7A.py  

## SG1M  
### Field Image  
![SG1M field overview image](wiki/img/SG1M-WholeView.png)  
Colors may vary.  

### Python Script1  
    $ ~/choreonoid/build/bin/choreonoid ~/choreonoid/ext/WRS2020SG/script/SG1M-AizuSpiderSA.py  

### Python Script2  
    $ ~/choreonoid/build/bin/choreonoid ~/choreonoid/ext/WRS2020SG/script/SG1M-Quadcopter.py  

## SG2  
### Field Image  
![SG2 field overview image](wiki/img/SG2-WholeView.png)  
Colors may vary.  

### Sample movies to show removing an obstacle pushing over a slope by each size robot.  
1. Removing the obstacle by a large size robot: [mp4(7.7MB)](wiki/img/SG2-RemovingObstacle-LargeRobot.mp4)
2. Removing the obstacle by a middle size robot: [mp4(26MB)](wiki/img/SG2-RemovingObstacle-MiddleRobot.mp4)

### Sample movies to show how to remove the angled rod correctly.  
1. Removing the angled rod by a large size robot: [mp4(5.7MB)](wiki/img/SG2-RemovingAngledRod-LargeRobot.mp4)
2. Removing the angled rod by a middle size robot: [mp4(13MB)](wiki/img/SG2-RemovingAngledRod-MiddleRobot.mp4)

### Python Script  
    $ ~/choreonoid/build/bin/choreonoid ~/choreonoid/ext/WRS2020SG/script/SG2-DoubleArmV7A.py  

Edited: 7th Feb. 2020
