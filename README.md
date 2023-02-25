# unity_tb3
This repository references the project of "https://github.com/DynoRobotics/UnityRos2" and provides a detailed tutorial on how to use it.

1.You can navigate to /Assets and run 'python3 start_editor.py' to start unity3d.
2.Go to  /Assets/Scenes in the Project window and double click on the Turtlebot3NavigationDemo.
3.Press the Play button to start the simulation.

You are able to control the turtlebot3_burger by keyborad or use the package: turtlebot3_teleop to send /cmd_vel command (this package can be downloaded in "https://github.com/ROBOTIS-GIT/turtlebot3")

In addition you can also use the scene for slam and navigation.
    Slam: 1.Launch turtlebot3_fake_node.launch.py    //base_scan:=scan
          2.launch slam_gmapping.launch.py           //https://github.com/Project-MANAS/slam_gmapping  && use_sim_time=true
          3.Save the map 'ros2 run nav2_map_server map_saver -f ~/map
         
    Navigation:
          1.References :"https://unity-ros2.readthedocs.io/en/latest/turtlebot3-navigation2.html"
          or
          2.ros2 launch turtlebot3_navigation2 navigation2.launch.py
          3.Use the package turtlebot3_unity_bringup under /docker/turtlebot3_navigation
            (ros2 launch turtlebot3_unity_bringup nav2_bringup_launch.py base_scan:=scan)
          4.You can click the botton 'Navigation2 Goal' in Rviz2 to send some navigation goals to the robot.
