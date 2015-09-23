

include_directories(${CMAKE_SOURCE_DIR}/src)

add_executable(bench bench.cpp randombytes.c)
target_link_libraries(bench tweetnacl tweetnacl++)

add_executable(test test.cpp randombytes.c)
target_link_libraries(test tweetnacl tweetnacl++)

