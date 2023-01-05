project(src)

aux_source_directory(${LIBIPC_PROJECT_DIR}/src SRC_FILES)

file(GLOB HEAD_FILES ${LIBIPC_PROJECT_DIR}/include/*.h)

add_library(${PROJECT_NAME} SHARED ${SRC_FILES} ${HEAD_FILES})

# set output directory
set_target_properties(${PROJECT_NAME}
	PROPERTIES
	ARCHIVE_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/lib"
	LIBRARY_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/lib"
	RUNTIME_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/bin")

# set version
set_target_properties(${PROJECT_NAME}
    PROPERTIES
    VERSION 1.2.0
    SOVERSION 3)

target_include_directories( ${PROJECT_NAME}
    PUBLIC ${LIBIPC_PROJECT_DIR}/include
)
