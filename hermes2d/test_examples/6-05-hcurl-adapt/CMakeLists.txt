project(P04-04-hcurl)

add_executable(${PROJECT_NAME} main.cpp)

set_property(TARGET ${PROJECT_NAME} PROPERTY COMPILE_FLAGS ${FLAGS})

target_link_libraries(${PROJECT_NAME} ${HERMES2D})

if(H2D_WITH_TESTS)
  add_subdirectory(tests)
endif(H2D_WITH_TESTS)
