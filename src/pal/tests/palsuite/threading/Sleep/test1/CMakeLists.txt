cmake_minimum_required(VERSION 2.8.12.2)

set(CMAKE_INCLUDE_CURRENT_DIR ON)

set(SOURCES
  Sleep.c
)

add_executable(paltest_sleep_test1
  ${SOURCES}
)

add_dependencies(paltest_sleep_test1 coreclrpal)

target_link_libraries(paltest_sleep_test1
  pthread
  m
  coreclrpal
)
