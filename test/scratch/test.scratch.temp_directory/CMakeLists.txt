
add_executable(test.scratch.temp_directory
    test.scratch.temp_directory.cpp
)

target_link_libraries(test.scratch.temp_directory
    xTests
)

target_compile_options(test.scratch.temp_directory PRIVATE
    $<$<OR:$<CXX_COMPILER_ID:Clang>,$<CXX_COMPILER_ID:AppleClang>,$<CXX_COMPILER_ID:GNU>>: -Werror -Wall -Wextra -pedantic>
    $<$<CXX_COMPILER_ID:MSVC>: /WX /W4>
)

