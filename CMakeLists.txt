cmake_minimum_required(VERSION 3.15)
cmake_policy(SET CMP0091 NEW)
set(CMAKE_MSVC_RUNTIME_LIBRARY "MultiThreaded$<$<CONFIG:Debug>:Debug>")
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

project(GoPlusPlus)

find_package(wxWidgets REQUIRED COMPONENTS net core base adv)

add_executable(GoPlusPlus)
target_sources(GoPlusPlus PRIVATE
  "src/canvas.h" "src/canvas.cpp"
  "src/frame.h" "src/frame.cpp"
  "src/game.h" "src/game.cpp"
  "src/main.cpp" "art/GoPlusPlus.rc")
target_compile_options(GoPlusPlus PRIVATE "$<$<CXX_COMPILER_ID:MSVC>:/utf-8>")
target_link_options(GoPlusPlus PRIVATE "$<$<CXX_COMPILER_ID:MSVC>:/subsystem:windows>")
include(${wxWidgets_USE_FILE})
target_link_libraries(GoPlusPlus ${wxWidgets_LIBRARIES})
