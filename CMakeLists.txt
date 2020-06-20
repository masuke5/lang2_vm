cmake_minimum_required(VERSION 3.13)
project(lang2_vm
    VERSION 1.0.0
    LANGUAGES C)

add_library(lang2_vm)
target_include_directories(lang2_vm PUBLIC include)
target_compile_features(lang2_vm PUBLIC c_std_11)
target_compile_definitions(lang2_vm PRIVATE NDEBUG)
target_compile_options(lang2_vm PRIVATE
    $<$<OR:$<C_COMPILER_ID:Clang>,$<C_COMPILER_ID:GNU>>: -Wall>
)

add_executable(lang2_vm_test)
target_link_libraries(lang2_vm_test lang2_vm)

add_subdirectory(src)
