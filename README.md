# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure
```
Step1:Initialize the robot, chassis, LED, and camera systems, and start video streaming.

Step 2 :Move the robot forward and change LED color.

Step 3 :Perform rotations and side movements with synchronized LED color changes.

Step 4 :Complete a final 360° rotation with an LED color update.

Step 5 :Stop the video stream and shut down the robot safely.
```
## Program
```
from robomaster import robot
import time

if _name_ == '_main_':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis

    ## Write your code here

from robomaster import robot
import time
from robomaster import camera

if name == 'main':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis
    ep_led = ep_robot.led
    ep_camera = ep_robot.camera

    print("Video streaming started.....")
    ep_camera.start_video_stream(display=True, resolution = camera.STREAM_360P)

    ep_chassis.move(x=2.55, y=0, z=0, xy_speed=0.9).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=0,effect="on")

    ep_chassis.move(x=0.4, y=0, z=80, xy_speed=0.8).wait_for_completed()
    ep_led.set_led(comp = "all",r=128,g=0,b=0,effect="on")

    ep_chassis.move(x=0.75, y=0, z=0, xy_speed=0.8).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=128,b=128,effect="on")

    ep_chassis.move(x=0.3, y=0, z=90, xy_speed=0.8).wait_for_completed()
    ep_led.set_led(comp = "all",r=225,g=0,b=0,effect="on")

    ep_chassis.move(x=1.5, y=0, z=0, xy_speed=0.8).wait_for_completed()
    ep_led.set_led(comp = "all",r=225,g=0,b=225,effect="on")

    ep_chassis.move(x=0, y=0, z=60, xy_speed=0.8).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=225,b=255,effect="on")

    ep_chassis.move(x=0, y=1.58, z=0, xy_speed=0.8).wait_for_completed()
    ep_led.set_led(comp = "all",r=128,g=0,b=0,effect="on")

    ep_chassis.move(x=0, y=0, z=48, xy_speed=0.8).wait_for_completed()
    ep_led.set_led(comp = "all",r=153,g=51,b=102,effect="on")

    ep_chassis.move(x=0, y=1.55, z=0, xy_speed=0.8).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=0,b=128,effect="on")

    ep_chassis.move(x=2.05, y=0, z=0, xy_speed=0.8).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=102,b=0,effect="on")
     
    ep_chassis.move(x=0, y=0, z=80, xy_speed=0.8).wait_for_completed()
    ep_led.set_led(comp = "all",r=153,g=51,b=0,effect="on")

    ep_chassis.move(x=0.65, y=0, z=0, xy_speed=0.8).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=0,effect="on")

    ep_chassis.move(x=0, y=0, z=360, xy_speed=0.8).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=255,effect="on")

    time.sleep(4)
    ep_camera.stop_video_stream()
    print("Stopped video streaming.....")

    ep_robot.close()


    
    ep_robot.close()
```
## MobileRobot Movement Image:

![robo](./img/robomaster.png)

Insert image here


<br/>
<br/>
<br/>
<br/>

## MobileRobot Movement Video:

Upload your video in Youtube and paste your video-id here

[![IMAGE ALT TEXT HERE](https://youtu.be/cpFY2gBTC1o?si=fEfkW47VBpLLC9F1)
![alt text](image.png)


<br/>
<br/>
<br/>
<br/>

## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.


<br/>
<br/>

```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
