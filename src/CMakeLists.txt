
cmake_minimum_required(VERSION 3.6)

project (aplayer)

# The version number.
set (aplayer_VERSION_MAJOR 1)
set (aplayer_VERSION_MINOR 0)

## GCC specifics
#if(CMAKE_COMPILER_IS_GNUCXX)
#  set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -pedantic -Wall -std=c++0x")
#  set(CMAKE_CXX_FLAGS_DEBUG "${CMAKE_CXX_FLAGS_DEBUG} -O0 -ggdb")
#endif()

## Visual Studio specifics
#if(MSVC)
#endif()

add_subdirectory(driver)
#add_subdirectory(lib)

# CPack
# build a CPack driven installer package
include (InstallRequiredSystemLibraries)
set (CPACK_RESOURCE_FILE_LICENSE
     "${CMAKE_CURRENT_SOURCE_DIR}/../License.txt")
set (CPACK_PACKAGE_VERSION_MAJOR "${aplayer_VERSION_MAJOR}")
set (CPACK_PACKAGE_VERSION_MINOR "${aplayer_VERSION_MINOR}")
include (CPack)

