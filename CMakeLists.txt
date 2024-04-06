cmake_minimum_required(VERSION 3.8)
project(ocs2_robotic_assets)

include_directories(include)

find_package(ament_cmake_auto REQUIRED)
ament_auto_find_build_dependencies()

ocs2_package()

configure_file (
  "${PROJECT_SOURCE_DIR}/include/${PROJECT_NAME}/package_path.hpp.in"
  "${PROJECT_SOURCE_DIR}/include/${PROJECT_NAME}/package_path.hpp" @ONLY
)

ament_auto_package()
