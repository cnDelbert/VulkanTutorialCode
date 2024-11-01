cmake_minimum_required(VERSION 3.29)
project(VulkanTutorial)

set(CMAKE_CXX_STANDARD 20)
set(Target VulkanTutorial)

set(GLFW_INCLUDE_DIR "deps/GLFW/include")
set(GLM_INCLUDE_DIR "deps/GLM")
set(VULKAN_INCLUDE_DIR "deps/Vulkan/Include")

include_directories(${GLFW_INCLUDE_DIR} ${GLM_INCLUDE_DIR} ${VULKAN_INCLUDE_DIR})

set(GLFW_LIB_DIR "deps/GLFW/lib_win64")
set(VULKAN_LIB_DIR "deps/Vulkan/Lib")

link_directories(${GLFW_LIB_DIR} ${VULKAN_LIB_DIR})

add_executable(${Target} main.cpp)
target_link_libraries(${Target} vulkan-1 glfw3)

