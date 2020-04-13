cmake_minimum_required(VERSION 3.1 FATAL_ERROR)

# Set project information
project(GoogleAssistantSDK VERSION 0.6.0 LANGUAGES CXX)
set(PROJECT_BRIEF "A cross-platform, modular SDK for interacting with the Google Assistant Service")
if (EXISTS "${CMAKE_CURRENT_SOURCE_DIR}/CapabilityAgents/ExternalMediaPlayer/src/ExternalMediaPlayerAdapters")
    set(HAS_EXTERNAL_MEDIA_PLAYER_ADAPTERS ON)
endif()

set(CMAKE_BINARY_DIR ${CMAKE_BINARY_DIR}/../build)
add_definitions(-D_GLIBCXX_USE_C99=1)

include(build/BuildDefaults.cmake)
include(tools/Testing.cmake)

# Set variables for target install and .pc pkg-config file
include(build/cmake/PrepareInstall.cmake)


configure_file (

        )


# Alexa Client SDK targets.


# Create .pc pkg-config file
include(build/cmake/GeneratePkgConfig.cmake)
