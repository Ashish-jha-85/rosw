cmake_minimum_required(VERSION 3.8)
project(task4c_3578)

# ---------------- Dependencies ----------------
find_package(ament_cmake REQUIRED)
find_package(rclpy REQUIRED)

# ---------------- Install Python nodes ----------------
install(
  PROGRAMS
    src/prescription.py
    src/task4A.py
    src/task4a_motion_check_real.py
    src/task4c_pre_run.py
  DESTINATION lib/${PROJECT_NAME}
)

# ---------------- Testing (optional) ----------------
if(BUILD_TESTING)
  find_package(ament_lint_auto REQUIRED)
  set(ament_cmake_copyright_FOUND TRUE)
  set(ament_cmake_cpplint_FOUND TRUE)
  ament_lint_auto_find_test_dependencies()
endif()

ament_package()
