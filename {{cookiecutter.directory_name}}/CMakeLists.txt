cmake_minimum_required(VERSION 3.9)
project({{cookiecutter.project_name}} CXX)

option(ENABLE_TESTING "" OFF)
if(ENABLE_TESTING)
    find_package(GTest REQUIRED)
    enable_testing ()
endif()

add_subdirectory(Library)
add_subdirectory(Demo)


