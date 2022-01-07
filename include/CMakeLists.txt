target_include_directories(plutovg
PUBLIC
    "${CMAKE_CURRENT_LIST_DIR}"
)

set_target_properties(plutovg PROPERTIES PUBLIC_HEADER plutovg.h)
target_compile_definitions(plutovg PRIVATE PLUTO_EXPORT_LIB)