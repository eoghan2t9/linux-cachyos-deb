# CachyOS Kernel Builder for Debian-based Distributions

<div align="center">
  <img src="https://github.com/CachyOS/calamares-config/raw/grub-3.2/etc/calamares/branding/cachyos/logo.png" width="64" alt="CachyOS logo"></img>
  <br/>
  <h1 align="center">CachyOS</h1>
  <p align="center">CachyOS provides enhanced kernels that offer improved performance and other benefits.</p>
</div>


This repository contains a TUI utility for building the Linux Kernel with various optimizations from CachyOS tailored to your system's CPU architecture. It automates the configuration and creates distributable Debian packages with these modifications.

# Features

The utility provides the following:

- Build a Linux Kernel using [patches from CachyOS](https://github.com/CachyOS/kernel-patches).
- Advanced configuration options, including compilation optimizations.
- Create distributable Debian packages.

# Usage

To use the utility, follow these steps:

1. Clone the repository to your local machine.
2. Make the utility executable with `chmod +x cachy-kernel-deb` and move the utility to a directory in the `$PATH`.
3. Run the utility with `cachy-kernel-deb` and follow the on-screen prompts to configure the kernel and build the packages.

# Advanced Configuration

The utility includes advanced configuration options for users who want to fine-tune their kernel:

- **Linux Kernel Configuration**: Choose from different configurations for the Linux Kernel from CachyOS.
- **CPU Scheduler**: Choose between various schedulers from CachyOS.
- **Configure LLVM's Link Time Optimization (LTO)**: Select from Thin and Full LTO for better optimization.
- **Configurable Tick Rate and Tick Types**: You can configure the kernel tick rate and types according to your system's needs.
- **Configurable NR_CPUS**: Set the maximum number of CPUs/cores the kernel will support.
- **Configurable Hugepages**: Enable Hugepages support or not.
- **Configurable LRU**: Configure the Least Recently Used memory management mechanism.
- **Configurable Preemption Type**: Kernel preemption types generally control how the Linux kernel handles tasks and interrupts, affecting system responsiveness and latency.
- **Configurable Kernel Name**: Choose a name for your custom kernel.
- **Additional Optimizations**: Optimizations target aspects of system performance and can provide benefits depending on the workload and system configuration.
    - **Use GCC -O3 Optimizations**: Aggressively optimizes compiled code for speed, possibly increasing binary size and compilation time.
    - **Enable Performance Governor**: This setting sets the CPU to run at maximum frequency, boosting performance but increasing power consumption and heat.
    - **Enable VMA Optimizations**: Enhances memory management efficiency, potentially improving application performance.
    - **Enable DAMON**: Monitors data access patterns to optimize memory usage and improve performance.
    - **Enable NUMA**: Optimizes memory allocation and access patterns on NUMA systems to reduce latency.

# Contributing

Contributions are welcome! If you have suggestions for improving the utility or adding new features, please open an issue or submit a pull request.

# License

The repository and its contents are licensed under BSD-3-Clause.

# Issues

If you find problems with the contents of this repository, please create an issue.

©2024 Laio O. Seman, Nitrux Latinoamericana S.C.
©2025 Nitrux Latinoamericana S.C.
