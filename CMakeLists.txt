# RIFT_IO_STANDARD_CMAKE_COPYRIGHT_HEADER(BEGIN)
# Author(s): Anil Gunturu
# Creation Date: 8/29/2013
# RIFT_IO_STANDARD_CMAKE_COPYRIGHT_HEADER(END)

cmake_minimum_required(VERSION 2.8)

include(GNUInstallDirs)
##
# Include the subdirs
##
set(subdirs
estw
  )
ADD_SUBDIRECTORY(${subdirs})
