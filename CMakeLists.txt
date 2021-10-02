cmake_minimum_required(VERSION 3.20)
set(CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

project(PolygonPoints)
find_package(SFML 2.5.1 COMPONENTS graphics window system audio REQUIRED)
file(
    GLOB
    SOURCES
    "src/*.hpp"
    "src/*.cpp"
)

add_executable(PolygonPoints ${SOURCES})
target_link_libraries(PolygonPoints sfml-graphics sfml-window sfml-system sfml-audio)
