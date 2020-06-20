cmake_minimum_required(VERSION 3.13)

target_sources(lang2_vm
    PRIVATE
    vm.c
)

target_sources(lang2_vm_test
    PRIVATE
    main.c
)
