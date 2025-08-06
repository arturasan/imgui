add_library(imgui SHARED
    imgui.cpp
    imgui_draw.cpp
    imgui_tables.cpp
    imgui_widgets.cpp
    imgui_demo.cpp
)
target_include_directories(imgui PUBLIC .)

# Add this block to place the .so file where the launcher can find it
set_target_properties(imgui PROPERTIES
    LIBRARY_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/launcher
)