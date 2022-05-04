PROJECT(New)

cmake_minimum_required(VERSION 2.4)
if(COMMAND cmake_policy)
  cmake_policy(SET CMP0003 NEW)
endif(COMMAND cmake_policy)

find_package(OpenIGTLink REQUIRED)

include(${OpenIGTLink_USE_FILE})

ADD_EXECUTABLE(NewClient  NewClient.cxx)
TARGET_LINK_LIBRARIES(NewClient OpenIGTLink)

ADD_EXECUTABLE(NewServer  NewServer.cxx)
TARGET_LINK_LIBRARIES(NewServer OpenIGTLink)
