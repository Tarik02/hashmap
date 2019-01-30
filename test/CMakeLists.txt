cmake_minimum_required(VERSION 3.5)
project(hashmap_test VERSION 1.0.0 LANGUAGES C)

add_executable(hashmap_test
    hashmap_test.c
)

target_compile_options(hashmap_test PRIVATE $<$<CXX_COMPILER_ID:GNU>:-Wall -Wunused -Werror>)

target_link_libraries(hashmap_test HashMap::HashMap)
