cmake_minimum_required(VERSION 3.12)
project(PackageTest CXX)


include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
conan_basic_setup()

add_executable(example example.cpp)
target_link_libraries(example PRIVATE ${CONAN_LIBS})
target_compile_features(example PRIVATE cxx_std_17)
