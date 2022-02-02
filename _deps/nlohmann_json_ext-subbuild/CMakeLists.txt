# Distributed under the OSI-approved BSD 3-Clause License.  See accompanying
# file Copyright.txt or https://cmake.org/licensing for details.

cmake_minimum_required(VERSION 3.22.2)

# We name the project and the target for the ExternalProject_Add() call
# to something that will highlight to the user what we are working on if
# something goes wrong and an error message is produced.

project(nlohmann_json_ext-populate NONE)



include(ExternalProject)
ExternalProject_Add(nlohmann_json_ext-populate
                     "UPDATE_DISCONNECTED" "False" "URL" "https://github.com/nlohmann/json/releases/download/v3.7.3/include.zip"
                    SOURCE_DIR          "/workspace/mcpelauncher-manifest/_deps/nlohmann_json_ext-src"
                    BINARY_DIR          "/workspace/mcpelauncher-manifest/_deps/nlohmann_json_ext-build"
                    CONFIGURE_COMMAND   ""
                    BUILD_COMMAND       ""
                    INSTALL_COMMAND     ""
                    TEST_COMMAND        ""
                    USES_TERMINAL_DOWNLOAD  YES
                    USES_TERMINAL_UPDATE    YES
)


