cmake_minimum_required(VERSION 3.28)
project(stb_image LANGUAGES CXX C)

add_library(
	stb_image STATIC
	"src/stb_image.c"
)

target_compile_features(stb_image PRIVATE c_std_11)

target_include_directories(
    stb_image SYSTEM PUBLIC
    "${PROJECT_SOURCE_DIR}/include"
)
