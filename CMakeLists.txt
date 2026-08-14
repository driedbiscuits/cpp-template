cmake_minimum_required(VERSION 3.15)
project(main C CXX)

set(CMAKE_C_STANDARD 23)
set(CMAKE_C_STANDARD_REQUIRED ON)
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(CMAKE_BUILD_TYPE RelWithDebInfo)


# ========== ADD SOURCE FILES HERE ==========
add_executable(main
    ${CMAKE_CURRENT_SOURCE_DIR}/src/main.cpp
)

# ========== ADD HEADER FILES HERE ==========
target_include_directories(main
    PUBLIC
        ${CMAKE_CURRENT_SOURCE_DIR}/include
    
    PRIVATE
        # private includes go here
)

# ========== ADD LINKED LIBRARIES HERE ==========
target_link_libraries(main
    PUBLIC
        # public libraries go here
    
    PRIVATE
        # private libraries go here
)

# ========== ADD COMPILER FLAGS HERE ==========
target_compile_options(main
    PUBLIC
        # public compile flags go here
        -O0
    
    PRIVATE
        # private compile flags go here
)