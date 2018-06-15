project(matplotlib_cpp)
cmake_minimum_required(VERSION 3.1)
set(CMAKE_CXX_STANDARD 14)
set(PYTHON_LIBRARY /usr/lib/x86_64-linux-gnu/libpython2.7.so)
set(PYTHON_INCLUDE_DIR /usr/include/python2.7)
find_package(PythonLibs 2.7 REQUIRED)

include_directories(${PYTHON_INCLUDE_DIRS})

add_executable(modern modern.cpp matplotlibcpp.h)

message(${PYTHON_LIBRARIES})
target_link_libraries(
modern
${PYTHON_LIBRARIES}
)
