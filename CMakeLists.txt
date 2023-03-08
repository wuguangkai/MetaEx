cmake_minimum_required(VERSION 3.17)
project(MetaEx)

set(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/output/bin)
set(LIBRARY_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/output/lib)

link_directories(${PROJECT_SOURCE_DIR}/thirdpart/fmt/lib)

include_directories(${PROJECT_SOURCE_DIR}/thirdpart/fmt/include)

set(libs fmt)

add_executable(MetaEx main.cpp)

target_link_libraries(${PROJECT_NAME} ${libs})