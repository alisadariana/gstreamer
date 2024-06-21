file(GLOB EXAMPLE_SOURCES *.c)

foreach(SOURCE_FILE ${EXAMPLE_SOURCES})
    get_filename_component(EXECUTABLE_NAME ${SOURCE_FILE} NAME_WE)

    add_executable(${EXECUTABLE_NAME} ${SOURCE_FILE})

    target_link_libraries(
        ${EXECUTABLE_NAME}
        PkgConfig::gstreamer
        PkgConfig::gtk
        PkgConfig::gstreamer-audio
        PkgConfig::gstreamer-pbutils
    )
endforeach()
