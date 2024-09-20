# 指定最低的 CMake 版本为 3.10
cmake_minimum_required(VERSION 3.10)

# 定义项目名称为 TEST1
project(TEST1)

# 设置 C++ 标准为 C++17
set(CMAKE_CXX_STANDARD 17)

# 设置可执行文件的输出路径为项目源目录下的 bin 文件夹
set(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin)

# 将当前目录下的所有源文件添加到 SRC_LISTS 变量中
aux_source_directory(. SRC_LISTS)

# 创建一个可执行文件 TEST1，使用 SRC_LISTS 中的源文件
add_executable(TEST1 ${SRC_LISTS})
