cmake_minimum_required(VERSION 2.6)
project(soil)

include_directories(include)

add_library(soil STATIC
    src/image_helper.c
    src/stb_image_aug.c
    src/image_DXT.c
    src/SOIL.c
)

install(DIRECTORY include/ DESTINATION include/)
install(TARGETS soil
    ARCHIVE DESTINATION lib
)
