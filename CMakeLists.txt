cmake_minimum_version(VERSION 3.10)

project(banking-system LANGUAGES C CXX)

set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

print("C flags: ${CMAKE_C_FLAGS}")
print("CXX flags: ${CMAKE_CXX_FLAGS}")
print("Using CMAKE_TOOLCHAIN_FILE=${CMAKE_TOOLCHAIN_FILE}")

include_directories(
  SYSTEM
  ${PROJECT_SOURCE_DIR}/include
)

add_subdirectory(src)

find_package(fmt CONFIG REQUIRED)
find_package(Boost.Asio CONFIG REQUIRED)


