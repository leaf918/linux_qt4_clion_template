cmake_minimum_required(VERSION 3.6)

project(test_qt_in_clion)
#qt
FIND_PACKAGE(Qt4 REQUIRED)
INCLUDE(${QT_USE_FILE})
INCLUDE_DIRECTORIES (${CMAKE_CURRENT_BINARY_DIR})
SET(QT_DONT_USE_QTGUI TRUE)
ADD_DEFINITIONS (${QT_DEFINITIONS})

#compile
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")
set(SOURCE_FILES main.cpp)
add_executable(test_qt_in_clion ${SOURCE_FILES})

TARGET_LINK_LIBRARIES(test_qt_in_clion ${QT_LIBRARIES})