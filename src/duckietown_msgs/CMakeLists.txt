cmake_minimum_required(VERSION 2.8.3)
project(duckietown_msgs)

find_package(catkin REQUIRED COMPONENTS
  roscpp
  rospy
  message_generation
  std_msgs
  geometry_msgs
  visualization_msgs
  sensor_msgs
  tf_conversions
  tf
)

## Generate messages in the 'msg' folder
add_message_files(
  FILES
  CarControl.msg
  CoordinationSignal.msg
  CoordinationSignalETHZ17.msg
  DuckieSensor.msg
  LanePose.msg

  IntersectionPose.msg
  IntersectionPoseImg.msg
  IntersectionPoseImgDebug.msg

  TurnIDandType.msg
#  LEDControl.msg
  LEDDetection.msg
  MaintenanceState.msg
  LEDDetectionArray.msg
  LEDDetectionDebugInfo.msg
  WheelsCmd.msg
  WheelsCmdStamped.msg
  Pose2DStamped.msg
  SignalsDetection.msg
  SignalsDetectionETHZ17.msg
  Twist2DStamped.msg
  Twist2DStampedETHZ17.msg
  AprilTagDetection.msg
  AprilTagDetectionArray.msg
  AprilTagsWithInfos.msg
  TagInfo.msg
  Pixel.msg
  Vector2D.msg
  Segment.msg
  SegmentList.msg
  Rect.msg
  Rects.msg
  SceneSegments.msg
  SourceTargetNodes.msg
  CoordinationClearance.msg
  CoordinationClearanceETHZ17.msg
#  IntersectionDetection.msg
#  CoordinationSignal.msg
#  TrafficLightDetection.msg
  VehicleCorners.msg
  VehiclePose.msg
#  VehicleDetection.msg
  FSMState.msg
  BoolStamped.msg
  BoolStampedETHZ17.msg
  StopLineReading.msg
  LEDInterpreter.msg
  AntiInstagramHealth.msg
  AntiInstagramTransform.msg
  AntiInstagramTransform_CB.msg
  KinematicsWeights.msg
  KinematicsParameters.msg
  ThetaDotSample.msg
  Vsample.msg
  Trajectory.msg
  ObstacleType.msg
  ObstacleImageDetection.msg
  ObstacleImageDetectionList.msg
  ObstacleProjectedDetection.msg
  ObstacleProjectedDetectionList.msg

)

## Generate services in the 'srv' folder
add_service_files(
  FILES
  SetFSMState.srv
  SetValue.srv
  SetVariable.srv
  GetVariable.srv
  # Service2.srv
)


## Generate added messages and services with any dependencies listed here
generate_messages(
  DEPENDENCIES
  std_msgs
  geometry_msgs
  sensor_msgs
)


catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES duckietown_msgs
   CATKIN_DEPENDS
   geometry_msgs
   roscpp rospy
   sensor_msgs
   std_msgs
   message_runtime
   visualization_msgs
#  DEPENDS system_lib
)


include_directories(
  ${catkin_INCLUDE_DIRS}
)
