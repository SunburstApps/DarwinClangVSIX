# Darwin Clang Support VSIX

This repository contains a Visual Studio extension that adds proper Darwin (macOS)
support to the Visual C++ Tools for Linux. The in-box targets are designed for GCC
and the GNU binutils linker. macOS uses Clang and the ld64 linker, and they are not
100% compatible with each other.

To use this extension with your C++ project, open the properties dialog for the
project (`*.vcxproj` file) you wish to use it with, and change the General > Platform
Toolset value to DarwinClang. Note that Darwin supports the x64 architecture only; if
you try to build with the x86 architecture (which is the default), this fact will be
detected and compiler error will occur.
