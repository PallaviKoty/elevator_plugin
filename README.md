# elevator_plugin

ROS package to control the lift car movement using ROS topic

Steps to use this package:
```
1. source /opt/ros/melodic/setup.bash
2. cd <elevator_plugin_ws/src>
3. git clone https://github.com/PallaviKoty/elevator_plugin.git
4. cd <elevator_plugin_ws>
5. catkin_make
6. source devel/setup.bash
```

To run gazebo with `elevator.world`,
```
7. roslaunch elevator_plugin launch_elevator.launch
```


To send the lift car to Level 1,
```
rostopic pub /elevator std_msgs/String "data: '1'" -1
```

To send the lift car to Level 0, 
```
rostopic pub /elevator std_msgs/String "data: '0'" -1
```

The `<door_wait_time>` is 10 sec. The plugin takes the request only after the current task is completed. There is no queue system implemented yet.




