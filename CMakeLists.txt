cmake_minimum_required(VERSION 3.21)
project(untitledmfkmkmk)
set(CMAKE_CXX_STANDARD 23)

add_executable(untitledmfkmkmk main.cpp)

install(TARGETS untitledmfkmkmk
        RUNTIME DESTINATION bin)

# ── CPack installer config ──────────────────────────────────────
set(CPACK_PACKAGE_NAME              "untitledmfkmkmk")
set(CPACK_PACKAGE_VERSION           "1.0.0")
set(CPACK_PACKAGE_VENDOR            "sahil")
set(CPACK_PACKAGE_DESCRIPTION_SUMMARY "My C++ Application")
set(CPACK_PACKAGE_INSTALL_DIRECTORY "untitledmfkmkmk")

# Windows NSIS
set(CPACK_NSIS_DISPLAY_NAME        "untitledmfkmkmk")
set(CPACK_NSIS_INSTALL_ROOT        "$PROGRAMFILES64")
set(CPACK_NSIS_MODIFY_PATH         ON)

# macOS DMG
set(CPACK_DMG_VOLUME_NAME          "untitledmfkmkmk")

# DEB (Ubuntu)
set(CPACK_DEBIAN_PACKAGE_MAINTAINER "sahilpadmani616@gmail.com")

# RPM (Fedora)
set(CPACK_RPM_PACKAGE_LICENSE      "MIT")

include(CPack)