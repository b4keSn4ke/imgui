cmake_minimum_required(VERSION 3.16.5)

project (imgui)

add_library(${PROJECT_NAME}
    imgui.h
    imgui.cpp
    imconfig.h
    imgui_demo.cpp
    imgui_draw.cpp
    imgui_internal.h
    imgui_tables.cpp
    imgui_widgets.cpp
    imstb_rectpack.h
    imstb_textedit.h
    imstb_truetype.h
)

# Adds -fPIC to compile command, seems to be needed for MakeFiles
set_target_properties(${PROJECT_NAME} PROPERTIES POSITION_INDEPENDENT_CODE ON)

target_include_directories(imgui
  PUBLIC ./
)
