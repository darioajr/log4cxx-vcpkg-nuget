# log4cxx.vcpkg

This NuGet package provides the **log4cxx** library, compiled with [vcpkg](https://github.com/microsoft/vcpkg) for **Windows x64** using **Microsoft Visual Studio 2022 (toolset v143)**.

[![Nuget Version](https://img.shields.io/nuget/v/log4cxx.vcpkg)](https://www.nuget.org/packages/log4cxx.vcpkg)

## 📦 Package Contents

- Header files (`include/log4cxx/*.h`)
- Static libraries:
  - `log4cxx.lib`
  - `charset.lib`
  - `iconv.lib`
  - `lzma.lib`
  - `zlib.lib` (or `zlibd.lib` in Debug mode)
- Dynamic libraries (`.dll`) for Debug and Release
- `.targets` file that automatically configures:
  - Include paths
  - Library paths
  - Dependencies
  - Copy `.dll` files to output folder (`$(OutDir)`)

## ⚙️ How to use

1. Add the package to your C++ project via NuGet.
2. Visual Studio will automatically apply the settings via the included `.targets` file.
3. Make sure your project is set to **x64** platform.

## 🔁 Automatic configuration

- In **Release**: links with `zlib.lib`
- In **Debug**: links with `zlibd.lib`
- DLLs are copied to `$(OutDir)` after build

## 📦 NuGet Package

- Available at: https://www.nuget.org/packages/log4cxx.vcpkg/

## 📝 License

- **log4cxx**: [Apache-2.0](https://spdx.org/licenses/Apache-2.0.html)
- This NuGet package: [Apache-2.0](https://spdx.org/licenses/Apache-2.0.html)

## 🔗 Useful Links

- Official site: https://logging.apache.org/log4cxx/
- Source: https://github.com/apache/logging-log4cxx
- vcpkg: https://github.com/microsoft/vcpkg