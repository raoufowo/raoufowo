cmake_minimum_required(VERSION 3.6)
project(raoufowo)
# Define your library
add_library(raoufowo raoufowo.cpp raoufowo.h)

# Set include directories for the library
target_include_directories(raoufowo PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})

# Install targets and files
install(TARGETS raoufowo
        EXPORT raoufowoTargets
        LIBRARY DESTINATION lib
        ARCHIVE DESTINATION lib
        RUNTIME DESTINATION bin
        INCLUDES DESTINATION include)

install(FILES raoufowo.h DESTINATION include)

# Install license file
install(FILES LICENSE DESTINATION share/raoufowo)

# Generate and install CMake configuration files
