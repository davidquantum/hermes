project(test-mesh_copy)

add_executable(${PROJECT_NAME} main.cpp)

set_property(TARGET ${PROJECT_NAME} PROPERTY COMPILE_FLAGS ${FLAGS})

target_link_libraries(${PROJECT_NAME} ${HERMES2D})

set(BIN ${PROJECT_BINARY_DIR}/${PROJECT_NAME})
add_test(test-mesh_copy-1 "${BIN}" domain.mesh 1)
add_test(test-mesh_copy-2 "${BIN}" bracket.mesh 1)
add_test(test-mesh_copy-3 "${BIN}" square.mesh 1)
add_test(test-mesh_copy-4 "${BIN}" square_tri.mesh 1)
add_test(test-mesh_copy_base-1 "${BIN}" domain.mesh 2)
add_test(test-mesh_copy_base-2 "${BIN}" bracket.mesh 2)
add_test(test-mesh_copy_base-3 "${BIN}" square.mesh 2)
add_test(test-mesh_copy_base-4 "${BIN}" square_tri.mesh 2)
add_test(test-mesh_copy_refine-1 "${BIN}" domain.mesh 3)
add_test(test-mesh_copy_refine-2 "${BIN}" bracket.mesh 3)
add_test(test-mesh_copy_refine-3 "${BIN}" square.mesh 3)
add_test(test-mesh_copy_refine-4 "${BIN}" square_tri.mesh 3)
