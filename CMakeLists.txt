cmake_minimum_required( VERSION 2.8 )
project( IsDoorOpen )
project( show_vals_on_door )

find_package( OpenCV REQUIRED )
find_package(Boost COMPONENTS system REQUIRED)
find_package( Curses REQUIRED )

include_directories( ${OpenCV_INCLUDE_DIRS} )
include_directories( ${Boost_INCLUDE_DIR} )
include_directories( ${CURSES_INCLUDE_DIR} )

add_executable( IsDoorOpen IsDoorOpen.cpp)

target_link_libraries( IsDoorOpen ${OpenCV_LIBS} )
target_link_libraries( IsDoorOpen ${Boost_SYSTEM_LIBRARY} )
target_link_libraries( IsDoorOpen ${CURSES_LIBRARIES} )


