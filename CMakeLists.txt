cmake_minimum_required(VERSION 3.17)
project(MetaEx)

set(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/output/bin)
set(LIBRARY_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/output/lib)

set(include_path ${PROJECT_SOURCE_DIR}/thirdpart/fmt/include
                 ${PROJECT_SOURCE_DIR}/thirdpart/pcap/include)

link_directories(${PROJECT_SOURCE_DIR}/thirdpart/fmt/lib)

include_directories(${include_path})

set(libs -lfmt -lpcap)

add_executable(MetaEx main.cpp capture/pcap_reader.h capture/pcap_reader.cpp)

target_link_libraries(${PROJECT_NAME} ${libs})