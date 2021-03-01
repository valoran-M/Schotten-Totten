cmake_minimum_required(VERSION 3.0)

project(Schotten-Totten VERSION 0.0.1)

find_package(doctest REQUIRED)
include(doctest)

set(SRCS
    
)

set(HEADERS

)

set(TESTS

)

set(LIBS
    ncuses
)

add_executable(Schotten-Totten src/main.cpp ${SRCS} ${HEADERS})
target_compile_features(Schotten-Totten PRIVATE cxx_std_17)
target_include_directories(Schotten-Totten PUBLIC src/)
target_link_libraries(Schotten-Totten ${LIBS})


add_executable(run_tests ${TESTS} ${SRCS} ${HEADERS})
target_compile_features(run_tests PRIVATE cxx_std_17)
target_include_directories(run_tests PUBLIC src/)
target_link_libraries(run_tests PRIVATE doctest::doctest ${LIBS})