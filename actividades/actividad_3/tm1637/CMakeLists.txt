add_library(tm1637 STATIC ${CMAKE_CURRENT_LIST_DIR}/tm1637.c)
pico_generate_pio_header(tm1637 ${CMAKE_CURRENT_LIST_DIR}/tm1637.pio)
target_include_directories(tm1637 PUBLIC ${CMAKE_CURRENT_LIST_DIR})
target_link_libraries(tm1637 PRIVATE pico_stdlib hardware_pio)