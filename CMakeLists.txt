# RIFT_IO_STANDARD_CMAKE_COPYRIGHT_HEADER(BEGIN)
# Author(s): Anil Gunturu
# Creation Date: 8/29/2013
# RIFT_IO_STANDARD_CMAKE_COPYRIGHT_HEADER(END)

cmake_minimum_required(VERSION 2.8)

##
# Include the subdirs
##
set(subdirs
estw
  )
rift_add_subdirs(SUBDIR_LIST ${subdirs})
