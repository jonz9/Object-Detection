cmake_minimum_required(VERSION 3.10)

project(ObjectDetection)

set(OpenCV_DIR C:/Users/zhang/Downloads/opencv/build)

find_package(OpenCV REQUIRED)

if(OpenCV_FOUND)
    message(STATUS "OpenCV version: ${OpenCV_VERSION}")
    message(STATUS "OpenCV include dirs: ${OpenCV_INCLUDE_DIRS}")
    message(STATUS "OpenCV libraries: ${OpenCV_LIBS}")
else()
    message(FATAL_ERROR "OpenCV was not found. Please check the OpenCV installation.")
endif()

# include_directories(${OpenCV_INCLUDE_DIRS})

add_executable(${PROJECT_NAME} src/Main.cpp)

target_link_libraries(${PROJECT_NAME} ${OpenCV_LIBS})
