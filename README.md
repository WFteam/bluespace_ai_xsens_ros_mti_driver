
# Description

This repo is a fork of [bluespace_ai_xsens_mti_driver](https://github.com/bluespace-ai/bluespace_ai_xsens_ros_mti_driver), and contains a stripped down version which only includes the XSens MT Software Suite SDK xspublic source files for interfacing with XSens MT imu devices with the `glyd` repo as a third party submodule.

Changelog from the original fork includes:

- Removing non-SDK artifacts (ROS files, CAD files)
- Move SDK lib sources to top level (e.g. everything in lib/xspublic)
- Add CMakeLists.txt for glyd repo building
- Fix C++20 errors/warnings
