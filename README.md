# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

#### Step1:
Use from robomaster import robot



#### Step2:

Choose the x,y,z - axis movement distance(meters).

#### Step3:

Give ep_chassis.move to move straight.

#### Step4:

Give time.sleep() for a break.

#### Step5:

Give ep_chassis.drive_speed to have a circular movement.

## Program
```python
from robomaster import robot
import time

if __name__ == '__main__':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis
    ep_led = ep_robot.led
    ep_camera = ep_robot.camera

    print("Video streaming started.....")
    ep_camera.start_video_stream(display=True, resolution = camera.STREAM_360P)

    ep_chassis.move(x=0.8, y=0, z=0, xy_speed=1.5).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=255,effect="on")

    ep_chassis.move(x=0, y=0, z=15, xy_speed=0).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=255,b=0,effect="on")
 
    ep_chassis.move(x=0, y=2.15, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=225,g=204,b=0,effect="on")

    ep_chassis.move(x=0, y=0, z=-8, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=51,b=102,effect="on")

    ep_chassis.move(x=-1.45, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=153,g=51,b=102,effect="on")

    ep_chassis.move(x=0, y=0, z=35, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=102,g=0,b=102,effect="on")

    ep_chassis.move(x=0, y=-1.5, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=0,b=255,effect="on")

    ep_chassis.move(x=0, y=0, z=135, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=51,g=102,b=255,effect="on")

    ep_chassis.move(x=1.5, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=204,b=0,effect="on")

    ep_chassis.move(x=0, y=0, z=110, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=153,g=51,b=102,effect="on")

    ep_chassis.move(x=-0.97, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=128,g=0,b=128,effect="on")

    ep_chassis.move(x=0, y=-0.6, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=204,g=255,b=255,effect="on")

    ep_chassis.move(x=0, y=0, z=72, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp = "all",r=128,g=128,b=0,effect="on")

    ep_chassis.move(x=2.35, y=0, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=153,g=51,b=0,effect="on")

    ep_chassis.move(x=0, y=0, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=0,b=0,effect="on")

    time.sleep(4)
    ep_camera.stop_video_stream()
    print("Stopped video streaming.....")#



    
    ep_robot.close()
```

## MobileRobot Movement Image:

![robo](./img/robomaster.png)

![WhatsApp Image 2023-12-28 at 17 27 08](https://github.com/Prajin19/mobilerobot-openloopcontrol/assets/144979377/18388a7a-c782-4d5e-8f4f-375d6e73c0d2)

![WhatsApp Image 2023-12-28 at 17 27 07](https://github.com/Prajin19/mobilerobot-openloopcontrol/assets/144979377/1011ef73-8d78-4a7b-9452-75a1d68b25a2)

![WhatsApp Image 2023-12-28 at 17 27 06](https://github.com/Prajin19/mobilerobot-openloopcontrol/assets/144979377/435b475e-53ee-49a5-8c93-879e4c238581)


## MobileRobot Movement Video:

https://youtu.be/ao98DlBlQ1s?si=ZgVMTkZGr4u0NBce

## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.


<br/>
<br/>

```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
