file(GLOB SOURCES *.c)
set(LVQRCODE_INCLUDE_DIRS .)

idf_component_register(SRCS ${SOURCES}
                       INCLUDE_DIRS ${LVQRCODE_INCLUDE_DIRS}
                       REQUIRES lvgl)

target_compile_definitions(${COMPONENT_LIB} PUBLIC "-DLV_LVGL_H_INCLUDE_SIMPLE")
