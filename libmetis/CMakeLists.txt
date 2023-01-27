

# Find sources.
file(GLOB metis_sources *.c)

# Build libmetis.
add_library(metis ${metis_sources})
find_package(gklib REQUIRED)
target_link_libraries(metis PUBLIC gklib::gklib)
target_include_directories(metis PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
target_include_directories(metis PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/../include)
