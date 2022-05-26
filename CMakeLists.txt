cmake_minimum_required(VERSION 3.14...3.23)

project(BoostFilesystem LANGUAGES CXX)

include(FetchContent)

FetchContent_Declare(
	boost
	GIT_REPOSITORY https://github.com/boostorg/boost.git
	GIT_TAG boost-1.79.0
)

# CMake 3.14 +
FetchContent_MakeAvailable(boost)

add_executable(filesys_example main.cpp)
target_link_libraries(filesys_example PRIVATE boost::filesystem)
