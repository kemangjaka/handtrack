cmake_minimum_required(VERSION 2.8)
project(MyOpenCVProject)

# Copy resouce


# Create Main project
set(SOURCES
    handtracker/main.cpp
    handtracker/Classifier.cpp
    handtracker/FeatureComputer.cpp
    handtracker/HandDetector.cpp
    handtracker/LcBasic.cpp
)

set(HEADERS
handtracker/Classifier.h
handtracker/FeatureComputer.hpp
handtracker/HandDetector.hpp
handtracker/LcBasic.h
)

add_executable(Main
    ${SOURCES}
    ${HEADERS}
)


# For OpenCV
find_package(OpenCV 2 REQUIRED)
if(OpenCV_FOUND)
    message(${OpenCV_INCLUDE_DIRS})
    target_include_directories(Main PUBLIC ${OpenCV_INCLUDE_DIRS})
    target_link_libraries(Main ${OpenCV_LIBS})
endif()