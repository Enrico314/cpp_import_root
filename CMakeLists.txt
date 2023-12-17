
# CMakeLists.txt for the "event" package. It creates a library and a main program.
# If ROOT is not installed in a default system location you need to tell CMake where to find it.
# Sourcing `thisroot.sh` already sets the required environment variables.
# Otherwise, you must tell the build system where to look for ROOT,
# for example by passing `-DROOT_DIR="/path/to/root/installation` at CMake configuration time.

project(bojara)
cmake_minimum_required(VERSION 3.0 FATAL_ERROR)
find_package(ROOT CONFIG REQUIRED)

add_executable(bojara main.cxx)

target_link_libraries(bojara PUBLIC ROOT::Hist ROOT::Core ROOT::Graf ROOT::Graf3d)



