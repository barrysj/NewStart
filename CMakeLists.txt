cmake_minimum_required(VERSION 2.8)
project(NewStart)

AUX_SOURCE_DIRECTORY(${PROJECT_SOURCE_DIR}/src SRC_LIST)

#指定头文件目录位置
#INCLUDE_DIRECTORIES(${PROJECT_SOURCE_DIR}/include)

#添加共享库搜索路径
#LINK_DIRECTORIES(${PROJECT_SOURCE_DIR}/lib)
SET(BUILD_OUTPUT_DIR ${PROJECT_SOURCE_DIR}/release)

#设置生成文件存放路径
SET(EXECUTABLE_OUTPUT_PATH ${BUILD_OUTPUT_DIR}/bin)
#SET(LIBRARY_OUTPUT_PATH ${BUILD_OUTPUT_DIR}/lib)

#生成可执行文件
ADD_EXECUTABLE(hello ${SRC_LIST})

#生成库文件
#ADD_LIBRARY(libhello ${SRC_LIST})

#设置target的属性
#set_target_properties(libhello PROPERTIES OUTPUT_NAME "hello")

#为hello添加共享库链接
#TARGET_LINK_LIBRARIES(hello math)

#执行子目录的CMakeLists.txt
#add_subdirectory(src)