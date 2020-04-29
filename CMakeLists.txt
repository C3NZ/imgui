cmake_minimum_required(VERSION 3.0.0)

project(imgui)

# Not needed anymore since the engine is now being compiled as a static
# lib.
# set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -fPIC")
include_directories(.)

set(
    IMGUI_SRC
    imconfig.h
    imgui.cpp
    imgui_demo.cpp
    imgui_draw.cpp
    imgui.h
    imgui_internal.h
    imgui_widgets.cpp
    imstb_rectpack.h
    imstb_textedit.h
    imstb_truetype.h
    )

add_library(imgui STATIC ${IMGUI_SRC})
