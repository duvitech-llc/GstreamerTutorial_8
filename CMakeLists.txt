# CMakeList.txt : Top-level CMake project file, do global configuration
# and include sub-projects here.
#
cmake_minimum_required (VERSION 3.8)

project ("GstreamerTutorial_8")

find_package(PkgConfig REQUIRED)

# Include sub-projects.
add_subdirectory ("GstreamerTutorial_8")

