# Demo
project(Demo CXX)

add_executable(${PROJECT_NAME} "")

target_sources(
    ${PROJECT_NAME}
    PUBLIC
    ${CMAKE_CURRENT_LIST_DIR}/src/main.cpp
)

target_include_directories(
    ${PROJECT_NAME}
    PUBLIC
    ${CMAKE_CURRENT_LIST_DIR}/include/
)

if(ENABLE_TESTING)
    add_subdirectory(test)
endif()
