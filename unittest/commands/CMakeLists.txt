
add_executable(test_simple_commands test_simple_commands.cpp)
target_link_libraries(test_simple_commands PRIVATE lammps GTest::GMock GTest::GTest)
add_test(NAME SimpleCommands COMMAND test_simple_commands WORKING_DIRECTORY ${CMAKE_CURRENT_BINARY_DIR})

add_executable(test_lattice_region test_lattice_region.cpp)
target_link_libraries(test_lattice_region PRIVATE lammps GTest::GMock GTest::GTest)
add_test(NAME LatticeRegion COMMAND test_lattice_region WORKING_DIRECTORY ${CMAKE_CURRENT_BINARY_DIR})

add_executable(test_kim_commands test_kim_commands.cpp)
target_link_libraries(test_kim_commands PRIVATE lammps GTest::GMock GTest::GTest)
add_test(NAME KimCommands COMMAND test_kim_commands WORKING_DIRECTORY ${CMAKE_CURRENT_BINARY_DIR})

add_executable(test_reset_ids test_reset_ids.cpp)
target_compile_definitions(test_reset_ids PRIVATE -DTEST_INPUT_FOLDER=${CMAKE_CURRENT_SOURCE_DIR})
target_link_libraries(test_reset_ids PRIVATE lammps GTest::GMock GTest::GTest)
add_test(NAME ResetIDs COMMAND test_reset_ids WORKING_DIRECTORY ${CMAKE_CURRENT_BINARY_DIR})
