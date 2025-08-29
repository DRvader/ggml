ggml_add_backend_library(ttx ggml-ttx.c)

if (APPLE)
target_link_libraries(ttx PRIVATE ${CMAKE_BINARY_DIR}/../../../../target/debug/libggml.dylib)
else()
target_link_libraries(ttx PRIVATE ${CMAKE_BINARY_DIR}/../../../../target/debug/libggml.so)
endif()
