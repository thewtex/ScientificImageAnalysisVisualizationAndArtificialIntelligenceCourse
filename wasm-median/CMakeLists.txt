cmake_minimum_required(VERSION 3.16)
project(median LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 20)

find_package(ITK REQUIRED COMPONENTS
  WebAssemblyInterface
)
include(${ITK_USE_FILE})

enable_testing()

# Begin create-itk-wasm added pipelines.
add_subdirectory(median-image-filter)

# End create-itk-wasm added pipelines.
