project(MS_Intersection)

cmake_minimum_required(VERSION 2.8)

find_package(OpenMP)
set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} ${OpenMP_C_FLAGS}")
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} ${OpenMP_CXX_FLAGS}")

aux_source_directory(. SRCS)

add_executable(MS_Intersection ${SRCS})

target_link_libraries(MS_Intersection ann)