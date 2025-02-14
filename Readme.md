# **Unity Drone Environments for RL**

<img src="./resrc/drone_flight_iso.gif" width="49%" />  <img src="./resrc/drone_juggling_iso.gif" width="49%" />

## **About**

There are drone environments made by **InSpace**. You can test your algorithm in these environments with default settings. Besides, you can change some settings(state, action, reward, ...) too. Most will be changed within __*DroneAgent.cs*__ script file. And You can make any environments with this drone agent. If you want to see another environments, click [here](https://www.youtube.com/channel/UCZx739AbunG2bGD5t0sNAhw/videos)

## **Environment** 

* Windows10 64bit
* Unity 2019.1.0f2 Personal
* Unity ML-Agents v0.8
* VisualStudio 2017

## **Drone Flight Environment**
<img src="./resrc/drone_flight_iso.gif" />

### Goal
 - To reach the white ball
 
### State
 - Vector from drone to ball
 - Up-vector of drone
 - Front-vector of drone
 - Velocity vector of drone
 - Angular velocity vector of drone

### Action
 - Value of each propellers thrust (Continuous)

### Reward
 - Δ(Distance from Drone to ball)

## **Drone Juggling Environment**
<img src="./resrc/drone_juggling_iso.gif" />

### Goal
 - To do not miss the red ball while flying

### State
 - Vector from drone to ball
 - Vecotr from current drone position to drone initial position
 - Up-vector of drone
 - Front-vector of drone
 - Velocity vector of drone
 - Angular velocity vector of drone
 - Normalized vector of Δ(ball position)
 
### Action
 - Value of each propellers thrust (Continuous)

### Reward
 - y-axis value of up-vector / CONSTANT
 - 1 / (CONSTANT + distance from current drone position to drone initial position)
 - 1 / (CONSTANT + distance from current ball position to ball initial position)

## **Getting Started**

### Change Setting & Make Environment
If you want to change setting(state, action, reward) or make new environment, open __*UnitySDK*__ with Unity.  
(Drone environments are located in __*Assets/DRONEENV*__.)  

If you need a tutorial about Unity ML-Agents, click [here](https://github.com/hyunho1027/Unity_ML_Agents_Tutorial)

### RL algorithm test
 You can test your algorithm with __*notebooks/getting-started.ipynb*__.

### Player Mode
 You can control the agent using a keyboard with __*playermodes/DRONEENV/DRONEENV.exe*__. 

### Player Control

| *Keyboard Key* | *Action* |
| --- | --- |
| Q | Thrust generation of the first propeller |
| W | Thrust generation of the second propeller |
| A | Thrust generation of the third propeller |
| S | Thrust generation of the fourth propeller |
