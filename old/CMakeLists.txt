project(octal)

if (NOT CMAKE_BUILD_TYPE)
    set(CMAKE_BUILD_TYPE "Release")
endif ()

if (UNIX)
    set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -march=native")
endif()

add_executable(analyze_exec src/analyze_exec.cc src/game.cc src/game_util.cc src/hadamard.cc src/game.h src/game_util.h src/hadamard.h)
