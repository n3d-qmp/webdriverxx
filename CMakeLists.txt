cmake_minimum_required(VERSION 3.0)
project(webdriverxx)
set(CMAKE_CXX_STANDARD 14)
set_property(TARGET webdriverxx PROPERTY COMPILE_WARNING_AS_ERROR ON)


enable_testing()

include_directories(include)
add_subdirectory(test)

install(DIRECTORY
		${CMAKE_SOURCE_DIR}/include/
		DESTINATION /usr/local/include/${PROJECT_NAME}
		FILES_MATCHING PATTERN "*")

