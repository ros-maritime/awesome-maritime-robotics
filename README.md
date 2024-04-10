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

## Control effort allocation / Thruster-managers
![pure_thrustallocation drawio (2)](https://github.com/bartboogmans/awesome-maritime-robotics/assets/5917472/82faf41e-1005-4574-a9df-bfa61f00853e)

Modules that attempt to best satisfy a reference resultant force by the ships actuators, given a certain thruster layout. The goal is to decide on actuator actions (generally either force $f=[f_1,...,f_n]$ or utilization $u = [u_1,...,u_n]^{\intercal}$ and orientations $\alpha = [\alpha_1,...,\alpha_n]^{\intercal}$) of all $n$ thrusters that combined satisfy desired resultant forces. In most cases (e.g. propellers, not fins) they relate by:

$$ \tau = T(\alpha)f(u) $$

Where the forces per actuator $f$ depends on utilization $u$ and $T$ is the thrust allocation matrix (which is constant if actuator angles $\alpha$ are static). 

- [MVP-Control](https://github.com/uri-ocean-robotics/mvp_control): A generic vehicle low-level vehicle controller (implements a control allocation algorithm with quadratic programming).
- [CentraleNantesROV thrust_manager](https://github.com/CentraleNantesROV/thruster_manager): Uses URDF to get thruster info. Method: predefined T inverse lookup ( $f=T^{-1} * \tau$ )
- [Robotic Decision Making Lab Oregon thrust manager](https://github.com/Robotic-Decision-Making-Lab/auv_controllers/tree/main/thruster_allocation_matrix_controller) Method: predefined T inverse lookup ( $f=T^{-1} * \tau$ )

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


## Planning/Guidance mission-planning:
- [MVP-Mission](https://github.com/uri-ocean-robotics/mvp_mission): A generic behavior-based state-oriented mission planner. It contains common behaviors for marine guidance.

## Actuator control
Modules that make sure that actuators follow a desired reference. Very vessel specific. 
- The [general ros2 control community](https://control.ros.org/master/index.html)

## Drivers
- [ping360_sonar](https://github.com/CentraleNantesRobotics/ping360_sonar)

## Open access datasets of marine drone operation
- [REMARO data](https://github.com/remaro-network/remaro_data)
