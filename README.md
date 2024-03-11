[![Build and Test](https://github.com/milliewalky/setup-cmake/actions/workflows/sample.yml/badge.svg)](https://github.com/milliewalky/setup-cmake/actions/workflows/sample.yml)

# Setup CMake

This action downloads, unpacks, and configures Cmake for use in GitHub Actions workflows. Perhaps everyone knows what CMake is, so I will not bother explaining it. CMake is unpacked under the temporary directory of a runner.

# Usage

<!-- start usage -->
```yaml
- uses: milliewalky/setup-cmake@v1
```
<!-- end usage -->

This action appends CMake to a temporary PATH file, so--for example--doing this in the root directory of your checked-out project:

```
(if exist build rmdir /s /q build) && mkdir build && cmake -S . -B build/ && cmake --build build/ --config Release
```

Should build it just fine.

# License

The scripts and documentation in this project are released under the [MIT License](LICENSE)
