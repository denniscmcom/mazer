cmake_minimum_required(VERSION 3.23)
project(mazer C)

set(CMAKE_C_STANDARD 99)

find_package(PNG REQUIRED)

add_executable(mazer
	src/main.c 
	src/algos.c 
	src/algos.h 
	src/process.c 
	src/process.h 
	src/handlers.c 
	src/handlers.h
)

target_include_directories(mazer PRIVATE ${PNG_INCLUDE_DIRS})
target_link_libraries(mazer ${PNG_LIBRARIES})

