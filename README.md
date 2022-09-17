# Motion Planning and Decision Making for Autonomous Vehicles

## Description

In this project, we will implement two of the main components of a traditional hierarchical planner: The Behavior Planner and the Motion Planner. <br>
Both will work in unison to be able to:

>- Avoid static objects (cars, bicycles and trucks) parked on the side of the road (but still invading the lane). The vehicle must avoid crashing with these vehicles by executing either a “nudge” or a “lane change” maneuver.
>- Handle any type of intersection (3-way, 4-way intersections and roundabouts) by STOPPING in all of them (by default)
>- Track the centerline on the traveling lane.

## Usage

Firstly, to use MotionPlanning, Carla simulator needs to be running in the background. 

Firsty unzip MotionPlanning/project/starter_files/lib.7z in order to be as follows:

>- MotionPlanning/project/starter_files/eigen-3.3.7
>- MotionPlanning/project/starter_files/libcarla-install
>- MotionPlanning/project/starter_files/rpclib


To do it, running the following commands:

```
su - student
// Will say permission denied, ignore and continue 
cd /opt/carla-simulator/
SDL_VIDEODRIVER=offscreen ./CarlaUE4.sh -opengl
```

Meanwhile, Carla Simulator is running in a dedicated prompt, compile and run MotionPlanning application using the following commands:

```
git clone https://github.com/hazemfahmyy/MotionPlanning.git
cd MotionPlanning/project
./install-ubuntu.sh
cd starter_files/
cmake .
make
cd MotionPlanning/project
./run_main.sh
// This might silently fail 
// ctrl + C to stop and restart
./run_main.sh again


// If error bind is already in use, or address already being used
ps -aux | grep carla
kill id
```
