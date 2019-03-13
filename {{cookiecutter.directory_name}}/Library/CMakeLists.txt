# Library
project(Library CXX)

add_library(${PROJECT_NAME} STATIC "")

target_sources(
    ${PROJECT_NAME}
    PUBLIC
    ${CMAKE_CURRENT_LIST_DIR}/include/${PROJECT_NAME}/Library.hpp
    ${CMAKE_CURRENT_LIST_DIR}/src/Library.cpp
)

target_include_directories(
    ${PROJECT_NAME}
    PUBLIC
    ${CMAKE_CURRENT_LIST_DIR}/include/
)

if(ENABLE_TESTING)
    add_subdirectory(test)
endif()
