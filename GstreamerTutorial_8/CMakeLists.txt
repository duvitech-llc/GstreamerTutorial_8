# CMakeList.txt : CMake project for GstreamerTutorial_1, include source and define
# project specific logic here.
#
cmake_minimum_required (VERSION 3.8)
pkg_check_modules(GSTLIBS REQUIRED
        gobject-2.0
        glib-2.0
        gstreamer-webrtc-1.0
        gstreamer-sdp-1.0
        gstreamer-pbutils-1.0
        libsoup-2.4
        json-glib-1.0
        gstreamer-rtsp-server-1.0
        gstreamer-check-1.0)


include_directories(${GSTLIBS_INCLUDE_DIRS})

link_directories(${GSTLIBS_LIBRARY_DIRS})

# Add source to this project's executable.
add_executable (GstreamerTutorial_8 "GstreamerTutorial_8.cpp" "GstreamerTutorial_8.h")

# TODO: Add tests and install targets if needed.
target_link_libraries(GstreamerTutorial_8 ${GSTLIBS_LIBRARIES})