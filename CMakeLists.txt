if(NOT ENABLE_GUI)
  return()
endif()

option(BUILD_uoa2020sg "Building the uoa2020sg files" ON)
if(NOT BUILD_uoa2020sg)
  return()
endif()

if(UNIX)
  add_custom_target(
    symlink_to_uoa2020sg ALL
    COMMAND ${CMAKE_COMMAND} -E create_symlink
    ${CMAKE_CURRENT_SOURCE_DIR} ${CNOID_BINARY_SHARE_DIR}/uoa2020sg)
endif()

install(DIRECTORY
  model
  project
  script
  DESTINATION ${CNOID_SHARE_SUBDIR}/uoa2020sg)

# add_subdirectory(controller)
