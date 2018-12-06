cmake_minimum_required(VERSION 3.7)
project(parallel_branch_and_bound)

SET(CMAKE_CXX_STANDARD 14)
SET(CMAKE_CXX_FLAGS_RELEASE "-fno-rtti -O3")
SET(CMAKE_CXX_FLAGS_DEBUG "-fno-rtti -O3")
SET(CMAKE_CXX_FLAGS "-std=c++14 -pthread")

set(SOURCE_FILES
        AlgorithmTest.cpp
        AlgorithmTest.h
        main.cpp
        TimeMeasurement.cpp
        TimeMeasurement.h
        TravellingSalesmanProblem.cpp
        TravellingSalesmanProblem.h
        TSPLIB_Parser.cpp TSPLIB_Parser.h ThreadPool.h)

add_executable(parallel_branch_and_bound ${SOURCE_FILES})