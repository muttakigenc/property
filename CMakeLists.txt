add_library(musProperty INTERFACE "includes/musProperty.h" "includes/musCheckOperator.h")

target_include_directories(musProperty
    INTERFACE
        ${CMAKE_CURRENT_SOURCE_DIR}/includes
)


if (CMAKE_VERSION VERSION_GREATER 3.8)
	set_property(TARGET musProperty PROPERTY CXX_STANDARD 23)
	set_property(TARGET musProperty PROPERTY CXX_STANDARD_REQUIRED ON)
	set_property(TARGET musProperty PROPERTY CXX_EXTENSIONS OFF)
endif()