project(mini-caffe C CXX)
cmake_minimum_required(VERSION 2.8)

include(mini-caffe.cmake)
#include(tests/tests.cmake)
#include(tools/tools.cmake)
file(GLOB INSTALL_HEAD_FILES ${CMAKE_SOURCE_DIR}/include/caffe/*.hpp)
install(TARGETS caffe 
        LIBRARY DESTINATION ${CMAKE_BINARY_DIR}/lib)
install(FILES ${INSTALL_HEAD_FILES} DESTINATION  ${CMAKE_INSTALL_PREFIX}/include/caffe)
