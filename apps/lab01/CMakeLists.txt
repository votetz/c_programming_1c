project("lab01")

file(GLOB SRC src/*.c)

include_directories(include)

add_executable(${PROJECT_NAME} ${SRC})

if (CMAKE_VERSION VERSION_GREATER 3.12)
  set_property(TARGET ${PROJECT_NAME} PROPERTY C_STANDARD 17)
endif()

target_link_libraries(${PROJECT_NAME} ${COMMON_LIB_DEPS}) 