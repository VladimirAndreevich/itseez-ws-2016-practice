set(target ${LIBRARY})

file(GLOB hdrs "*.h*")
file(GLOB srcs "*.cpp")

add_library(${target} STATIC ${srcs} ${hdrs})
target_link_libraries(${target} ${LIBRARY_DEPS})

set(LIBRARY_DEPS "${LIBRARY_DEPS};${target}" PARENT_SCOPE)
