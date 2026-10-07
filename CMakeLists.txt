cmake_minimum_required(VERSION 3.16)

project(PacketAnalyzer VERSION 1.0)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

set(SOURCES
    src/main_dpi.cpp
    src/dpi_engine.cpp
    src/pcap_reader.cpp
    src/packet_parser.cpp
    src/rule_manager.cpp
    src/connection_tracker.cpp
    src/fast_path.cpp
    src/load_balancer.cpp
    src/sni_extractor.cpp
    src/types.cpp
)

include_directories(${CMAKE_SOURCE_DIR}/include)

add_executable(dpi_engine ${SOURCES})