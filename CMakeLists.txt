cmake_minimum_required(VERSION 3.10 FATAL_ERROR)

# set the project name and version
# NOTE: `project` automatically defines `PROJECT_NAME` and `PROJECT_SOURSE_DIR`
project(MyTestProject VERSION 1.0)

# Add subdirectory
add_subdirectory(lib)

# Generate executable
add_executable(MyTestProject sample.cpp)

# linking
target_link_libraries(MyTestProject PRIVATE lib1)

# add the lib file into to the include path
target_include_directories(MyTestProject PRIVATE "${PROJECT_SOURCE_DIR}/lib")
