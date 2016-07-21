#
# Copyright 2016 RIFT.IO Inc
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
#
# Creation Date: Thu Mar 19 13:20:43 IST 2015
#

cmake_minimum_required(VERSION 2.8)

set(PKG_NAME estw)
set(PKG_VERSION 1.0)
set(PKG_RELEASE 1)
set(PKG_LONG_NAME ${PKG_NAME}-${PKG_VERSION})

##
# This appends to the list of directories to search for
# header files. INCLUDE_DIRECTORIES is a DIRECTORY property and
# is inherited from the parent directory.
#
include_directories(BEFORE
  include
  ../safe_base/include
  ${CMAKE_CURRENT_BINARY_DIR})

set(LIB_SOURCES
  src/stw_system_timer.c
  src/stw_timer.c
  )
##
# Add the target for the estw static library
##
add_library(estw SHARED ${LIB_SOURCES})

##
# The following code installs the targets to
# ${CMAKE_INSTALL_PREFIX}/usr/bin.
# Always use relative path for destination.
set(INSTALL_HFILES
  include/stw_system_timer.h
  include/stw_system_timer.h
  include/stw_timer.h
  ../safe_base/include/safe_limits.h  
  ../safe_base/include/safe_types.h
  )
install(FILES ${INSTALL_HFILES} DESTINATION ${CMAKE_INSTALL_INCLUDEDIR} COMPONENT ${PKG_LONG_NAME})
install(TARGETS estw LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR} COMPONENT ${PKG_LONG_NAME})

