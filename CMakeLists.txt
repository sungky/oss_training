cmake_minimum_required(VERSION 3.0.2)
project(team11)

find_package(catkin REQUIRED COMPONENTS
  rospy
)


catkin_python_setup()


## Generate messages in the 'msg' folder
# add_message_files(
#   FILES
#   Message1.msg
#   Message2.msg
# )

## Generate services in the 'srv' folder
# add_service_files(
#   FILES
#   Service1.srv
#   Service2.srv
# )

## Generate actions in the 'action' folder
# add_action_files(
#   FILES
#   Action1.action
#   Action2.action
# )

## Generate added messages and services with any dependencies listed here
# generate_messages(
#   DEPENDENCIES
#   std_msgs  # Or other packages containing msgs
# )


catkin_package(
CATKIN_DEPENDS rospy

)


#############
## Install ##
#############

catkin_install_python(PROGRAMS
  node/init_pose.py
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)

