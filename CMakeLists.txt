set(srcs
    "AccelStepper.cpp"
    "MultiStepper.cpp")

idf_component_register(SRCS "${srcs}"
                    REQUIRES "esp_driver_gpio esp_timer"
                    INCLUDE_DIRS include)

target_link_libraries(${COMPONENT_LIB} INTERFACE "-Wl,--undefined=uxTopUsedPriority")