# universal_robot

roslaunch ur_calibration calibration_correction.launch robot_ip:=192.168.0.102 target_filename:="${HOME}/my_robot_calibration.yaml"

roslaunch ur_robot_driver ur5_bringup.launch robot_ip:=192.168.0.102

START THE ROBOT!
 
roslaunch ur_robot_driver ur5_bringup.launch robot_ip:=192.168.0.102 kinematics_config:=$(rospack find ur_calibration)/etc/ur5_calibration.yaml

roslaunch ur_robot_driver ur5_bringup.launch robot_ip:=192.168.0.102 [reverse_port:=REVERSE_PORT] kinematics_config:="${HOME}/my_robot_calibration.yaml"

MOVE IT!

roslaunch ur5_moveit_config ur5_moveit_planning_execution.launch

roslaunch ur5_moveit_config moveit_rviz.launch config:=true

Verificar que este selecionado el manipulador en el goal state
