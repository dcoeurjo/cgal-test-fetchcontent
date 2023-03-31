project(cgal-test-fetchcontent)
cmake_minimum_required(VERSION 3.14)

message(STATUS "Third-party (external): creating CGAL targets")

include(FetchContent)
FetchContent_Declare(
     CGAL
     GIT_REPOSITORY https://github.com/CGAL/cgal.git
     GIT_TAG v5.5.2
     GIT_SHALLOW TRUE
     )
FetchContent_MakeAvailable(CGAL)

add_executable(for_loop_2 for_loop_2.cpp)
target_link_libraries(for_loop_2 CGAL::CGAL CGAL::CGAL_Core)
