# CachyOS Kernel Builder

This repository contains a script for building the CachyOS kernel with various optimizations tailored to your system's CPU architecture. The script automates the configuration and optimization of the kernel build according to your hardware and preferences.

# Prerequisites

Before running the script, ensure you have the following prerequisites installed:

- `gcc`: The GNU Compiler Collection is necessary to detect the CPU architecture.
- `whiptail`: For displaying dialog boxes in the script.
- `curl`: To fetch the latest kernel version.

You can install these dependencies using your distribution's package manager.

# Features

The script offers a variety of configuration options:

- Auto-detection of CPU architecture for optimization.
- Selection of CachyOS-specific optimizations.
- Configuration of CPU scheduler, LLVM LTO, tick rate, and more.
- Support for multiple kernel configurations such as NUMA, NR_CPUS, Hugepages, and LRU.
- Application of O3 optimization and performance governor settings.

# Usage

To use the script, follow these steps:

1. Clone the repository to your local machine.
2. Make the script executable with `chmod +x cachy-kernel-deb`.
3. Run the script with `bash cachy-kernel-deb`.

   3.1. Follow the on-screen prompts to select your desired kernel version and configurations, for:
      - Choose the kernel version.
      - Enable or disable CachyOS optimizations.
      - Configure the CPU scheduler, LLVM LTO, tick rate, NR_CPUS, Hugepages, LRU, and other system optimizations.
      - Select the preempt type and tick type for further system tuning.

4. Run the script with `bash cachy0kernel-deb -b` to build a Debian package.

To build an already configured kernel, follow these steps:

1. Enter the source directory of the Linux kernel.
2. Run the script with `bash cachy-kernel-deb`.

# Advanced Configuration

The script includes advanced configuration options for users who want to fine-tune their kernel:

- **CachyOS Configuration**: Enable optimizations specific to CachyOS.
- **CPU Scheduler**: Choose between several schedulers like Cachy, PDS, or none.
- **LLVM LTO**: Select from Thin and Full LTO for better optimization.
- **Tick Rate**: Configure the kernel tick rate according to your system's needs.
- **NR_CPUS**: Set the maximum number of CPUs/cores the kernel will support.
- **Hugepages**: Enable Hugepages support or not.
- **LRU**: Configure the Least Recently Used memory management mechanism.
- **O3 Optimization**: Apply O3 optimization for performance improvement.
- **Performance Governor**: Set the CPU frequency scaling governor to performance.

# Contributing

Contributions are welcome! If you have suggestions for improving the script or adding new features, please open an issue or submit a pull request.

# License

This project is licensed under the MIT License - see the LICENSE file for details.


# Issues
If you find problems with the contents of this repository please create an issue.

©2024 Nitrux Latinoamericana S.C.
