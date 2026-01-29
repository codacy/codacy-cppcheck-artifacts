# Codacy Cppcheck Artifacts

This repository builds [Cppcheck](https://github.com/danmar/cppcheck) from source and publishes pre-built binaries for multiple platforms.

## Supported Platforms

| Platform | Architecture | Artifact |
|----------|--------------|----------|
| Linux | x64 | `cppcheck-linux-x64-<version>.tar.gz` |
| Linux | ARM64 | `cppcheck-linux-arm64-<version>.tar.gz` |
| macOS | ARM64 | `cppcheck-macos-arm64-<version>.tar.gz` |

## Build Configuration

Cppcheck is built with the following options:

- **HAVE_RULES=ON** - PCRE regex rules support enabled
- **USE_MATCHCOMPILER=ON** - Match compiler optimization enabled
- **BUILD_GUI=OFF** - GUI not included
- **BUILD_TESTS=OFF** - Tests not included

Each artifact includes:
- The `cppcheck` binary
- Configuration files (`cfg/`)
- Addons (`addons/`)

## Updating Cppcheck Version

To update to a new Cppcheck version, modify the `.tool_version` file with the desired version number (e.g., `2.19.0`).

## Releases

Releases are automatically created when changes are pushed to the `main` branch. Each release is tagged with the Cppcheck version (e.g., `v2.19.0`).

## License

Cppcheck is licensed under the [GPLv3](https://github.com/danmar/cppcheck/blob/main/COPYING).
