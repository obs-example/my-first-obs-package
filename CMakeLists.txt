CMAKE_MINIMUM_REQUIRED( VERSION 2.8 )

set( PROJECT "hello-obs" )

project(${PROJECT})

# SET( PROJECT "hello-obs" )
set( YPREFIX "/usr" )

set( VERSION_MAJOR "0")
set( VERSION_MINOR "1" )
set( VERSION_PATCH "0" )
set( VERSION "${VERSION_MAJOR}.${VERSION_MINOR}.${VERSION_PATCH}${GIT_SHA1_VERSION}" )

set( SOURCE_FILES src/main.cpp )

add_definitions(-DVERSION="${VERSION}")

add_executable( ${PROJECT} ${SOURCE_FILES} )

install (TARGETS ${PROJECT} DESTINATION bin)
