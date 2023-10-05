# awesome-maritime-robotics
Repo for mapping all the open source robotics software, including the ones from this organization

## Simulation environments
### Gazebo
- [VRX Boat Simulation](https://github.com/osrf/vrx) gazebosim example.
- [Bluerov2](https://github.com/clydemcqueen/bluerov2_ignition) gazebosim model.
- [LRAUV](https://github.com/osrf/lrauv) gazebosim example. Contains DVL.
- [Orca4](https://github.com/clydemcqueen/orca4)
- [SUAVE](https://github.com/kas-lab/suave/blob/main/README.md) An Exemplar for Self-Adaptive Underwater Vehicles
- [REMARO Summer School Delft 2022 - Underwater robotics hackathon](https://github.com/remaro-network/tudelft_hackathon)
- [MBZIRC](https://github.com/osrf/mbzirc) Boat and aerial drone simulation. Contains radar.

### Other
- [Stonefish](https://stonefish.readthedocs.io/en/latest/) is a C++ library combining a physics engine and a lightweight rendering pipeline.
- [TurtleBoat](https://github.com/bartboogmans/TurtleBoat) is an interactive node, similar to turtlebot, but then with vessel dynamics

## Actuator control
Modules that make sure that actuators follow a desired reference. 
- The [general ros2 control community](https://control.ros.org/master/index.html)

## Motion control modules
Components that attempt to control the vessels motion to follow a reference state. 

### Dynamical positioning / station keeping
Full control over the pose of the vessel, generally for slow positioning, docking or station-keeping
- ...

### Heading / Velocity control
Approaches that are tailored to function with high surge speed, commonly neglecting drift and actuation in sway direction. 
- ...

### Other approaches
- ...

## Control effort allocation / Thruster-managers
Modules that attempt to best satisfy a reference resultant force by the ships actuators, given a certain thruster layout. 
- [MVP-Control](https://github.com/uri-ocean-robotics/mvp_control): A generic vehicle low-level vehicle controller (implements a control allocation algorithm with quadratic programming).

## Planning/Guidance mission-planning:
- [MVP-Mission](https://github.com/uri-ocean-robotics/mvp_mission): A generic behavior-based state-oriented mission planner. It contains common behaviors for marine guidance.

## Drivers
- [ping360_sonar](https://github.com/CentraleNantesRobotics/ping360_sonar)

## Open access datasets of marine drone operation
- [REMARO data](https://github.com/remaro-network/remaro_data)
