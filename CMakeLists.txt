cmake_minimum_required (VERSION 3.10)

project (hello-beast)

find_package(Boost COMPONENTS system thread REQUIRED)
find_package(Threads REQUIRED)

include_directories(${Boost_INCLUDE_DIRS})

add_executable (hello-beast "hello-beast.cpp")

target_link_libraries(hello-beast PRIVATE ${Boost_SYSTEM_LIBRARY} ${Boost_THREAD_LIBRARY} ${CMAKE_THREAD_LIBS_INIT})