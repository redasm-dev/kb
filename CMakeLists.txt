cmake_minimum_required(VERSION 3.25)
project(redasm-kb NONE)  # NONE = no compiler needed, it's just data files

if(WIN32)
    set(REDASM_INSTALL_KB "kb")
else()
    include(GNUInstallDirs)
    set(REDASM_INSTALL_KB "${CMAKE_INSTALL_DATADIR}/redasm/kb")
endif()

install(
    DIRECTORY "${CMAKE_CURRENT_SOURCE_DIR}/"
    DESTINATION ${REDASM_INSTALL_KB}
    FILES_MATCHING
            PATTERN "*.toml"
            PATTERN ".*" EXCLUDE
)
