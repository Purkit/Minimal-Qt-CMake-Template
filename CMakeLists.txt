cmake_minimum_required(VERSION 3.16)

project(PDFEditor VERSION 1.0.0 LANGUAGES CXX)


set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(Qt6 REQUIRED COMPONENTS Core Widgets)
qt_standard_project_setup()

add_subdirectory(src/app)

qt_add_resources(
    editor
    "resources"
    PREFIX "/Resources"
    BASE "${CMAKE_CURRENT_SOURCE_DIR}/res"
    FILES
        res/home.png
)
