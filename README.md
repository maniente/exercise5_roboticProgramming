# EXERCISE 5
## Task 1
```
gazebo exe5_world.world
```

## Task 2
```
export TURTLEBOT3_MODEL=burger
ros2 launch  turtlebot3_gazebo exe5_world.launch.py
ros2 launch turtlebot3_cartographer cartographer.launch.py use_sim_time:=True
ros2 run turtlebot3_teleop teleop_keyboard
ros2 run nav2_map_server map_saver_cli -f ~/map

```

## Task 3
launch the world again
```
export TURTLEBOT3_MODEL=burger2
ros2 launch turtlebot3_navigation2 navigation2.launch.py use_sim_time:=True map:=$HOME/Desktop/ex5/map_5.yaml

```

## Task 4
Repeat Task 2 but instead to use teleop use 
```
export TURTLEBOT3_MODEL=burger2
ros2 run turtlebot3_control exploration 

```

