cmake_minimum_required (VERSION 3.8)

set(HEADER_FILES include/glad/glad.h include/KHR/khrplatform.h)

add_library(glad
	src/glad.c

	${HEADER_FILES}
)

target_include_directories(glad PRIVATE include/)
target_compile_options(glad -fPIC)

install(TARGETS glad DESTINATION lib)
install(FILES include/glad/glad.h DESTINATION include/glad/)