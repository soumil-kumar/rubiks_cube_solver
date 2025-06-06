cmake_minimum_required(VERSION 3.31)
project(RUBIKS_CUBE_SOLVER)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED True)

include_directories(
    ${PROJECT_SOURCE_DIR}/Model
    ${PROJECT_SOURCE_DIR}/PatternDatabases
    ${PROJECT_SOURCE_DIR}/Solver
)

set(SOURCES
    main.cpp

    # Model
    Model/RubiksCube.cpp
    Model/RubiksCube1dArray.cpp
    Model/RubiksCube3dArray.cpp
    Model/RubiksCubeBitboard.cpp

    # PatternDatabases
    PatternDatabases/PatternDatabase.cpp
    PatternDatabases/CornerDBMaker.cpp
    PatternDatabases/CornerPatternDatabase.cpp
    PatternDatabases/Math.cpp
    PatternDatabases/NibbleArray.cpp
)

add_executable(rubik_cube_solver ${SOURCES})