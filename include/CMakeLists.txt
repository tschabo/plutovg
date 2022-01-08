target_include_directories(plutovg
PUBLIC
    "${CMAKE_CURRENT_LIST_DIR}"
)

target_sources(plutovg
    PUBLIC ${CMAKE_CURRENT_LIST_DIR}/plutovg.h
)

set_target_properties(plutovg PROPERTIES PUBLIC_HEADER ${CMAKE_CURRENT_LIST_DIR}/plutovg.h)
target_compile_definitions(plutovg PRIVATE PLUTO_EXPORT_LIB)