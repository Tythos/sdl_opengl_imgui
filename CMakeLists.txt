cmake_minimum_required(VERSION 3.14)
project(sdl_opengl_imgui)
add_subdirectory("sdl/" EXCLUDE_FROM_ALL)
add_executable(${PROJECT_NAME}
    "main.cpp"
    "imgui/imgui.cpp"
    "imgui/imgui_demo.cpp"
    "imgui/imgui_draw.cpp"
    "imgui/imgui_tables.cpp"
    "imgui/imgui_widgets.cpp"
    "imgui/backends/imgui_impl_sdl2.cpp"
    "imgui/backends/imgui_impl_opengl3.cpp"
)
target_include_directories(${PROJECT_NAME} PRIVATE
    "imgui/"
    "imgui/backends/"
)
target_link_libraries(${PROJECT_NAME} PRIVATE
    SDL2::SDL2
    SDL2::SDL2main
    OpenGL32
)
