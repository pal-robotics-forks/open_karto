cmake_minimum_required(VERSION 2.8)

#
# Copyright 2010 SRI International
# Copyright 2014 PAL Robotics
#
# This program is free software: you can redistribute it and/or modify
# it under the terms of the GNU Lesser General Public License as published by
# the Free Software Foundation, either version 3 of the License, or
# (at your option) any later version.
#
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU Lesser General Public License for more details.
#
# You should have received a copy of the GNU Lesser General Public License
# along with this program.  If not, see <http://www.gnu.org/licenses/>.
#

project(open_karto)

catkin_package(
    LIBRARIES OpenKarto
    INCLUDE_DIRS include
)

include_directories(include)


if(WIN32)
  # turn off various warnings
  foreach(warning 4251)
    SET(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} /wd${warning}")
  endforeach(warning)
endif()

# setup kt target
add_library(OpenKarto
    src/Karto.cpp
    src/Mapper.cpp
)

install(DIRECTORY include/${PROJECT_NAME}/
  DESTINATION ${CATKIN_PACKAGE_INCLUDE_DESTINATION}
  FILES_MATCHING PATTERN "*.h")

install(TARGETS OpenKarto DESTINATION ${CATKIN_PACKAGE_LIB_DESTINATION})
