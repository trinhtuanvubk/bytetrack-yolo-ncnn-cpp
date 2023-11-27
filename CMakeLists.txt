cmake_minimum_required(VERSION 3.12)
project(bytetrack)
set(CMAKE_CXX_STANDARD 14)
set(CMAKE_BUILD_TYPE Debug)

set(ncnn_DIR "/home/vutt/etc-workspace/cpp/ncnn/build/install/lib/cmake/ncnn" CACHE PATH "Directory that contains ncnnConfig.cmake")
find_package(OpenCV 4 REQUIRED)
find_package(ncnn REQUIRED)

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/../src)
include_directories(${CMAKE_CURRENT_BINARY_DIR}/../src)
include_directories(include)
include_directories(/usr/local/include/eigen3)
file(GLOB My_Source_Files src/*.cpp)

# Add an executable target
add_executable(${PROJECT_NAME} ${My_Source_Files})

target_link_libraries(${PROJECT_NAME} ${OpenCV_LIBS})
target_link_libraries(${PROJECT_NAME} ncnn)