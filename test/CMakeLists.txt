file(GLOB SOURCE_FILES CONFIGURE_DEPENDS *.cc)

add_executable(example-test ${SOURCE_FILES})
target_link_libraries(example-test catch)

add_test(example-test example-test)
