# ArgParserCC
Command line argument parser for C++

This project aims to provide a simple argument parser that can work for many different projects.

## Building Examples
`cd` into the example directory you want to build. 
Run the CMake setup command and then run CMake to build the example.

### Example build commands for show_help example
```shell
cd examples/show_help
cmake -S. -B ./build -D CMAKE_BUILD_TYPE=Release
cmake --build ./build -j1
```