
qt_add_executable(editor
    mainwindow.ui
    mainwindow.cpp
    main.cpp
)

target_link_libraries(editor PRIVATE Qt6::Widgets)

set_target_properties(editor PROPERTIES
    WIN32_EXECUTABLE ON
    MACOSX_BUNDLE ON
)
