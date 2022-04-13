cmake_minimum_required(VERSION 3.20)
project(perf_reshade)

add_subdirectory(thirdparty)

set(CMAKE_CXX_STANDARD 17)

set(SOURCE_FILES
        src/library.cpp
        )

# set options before add_subdirectory
# available options: TRACY_ENABLE , TRACY_ON_DEMAND , TRACY_NO_BROADCAST , TRACY_NO_CODE_TRANSFER , ...
#option(TRACY_ENABLE "" OFF)
#option(TRACY_ON_DEMAND "" OFF)
#add_subdirectory(3rdparty/tracy) # target: TracyClient or alias Tracy::TracyClient Link Tracy::TracyClient to any target where you use Tracy for profiling:

include_directories(${RESHADE_INCLUDE} ${TRACY_INCLUDE} include)

add_library(perf_reshade SHARED ${SOURCE_FILES})
#target_link_libraries(perf_reshade PUBLIC Tracy::TracyClient)
