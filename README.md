# CachyOS Kernel Builder for Debian-based Distributions

<div align="center">
  <img src="https://wiki.cachyos.org/_astro/logo.BL2wM24g_Z1ms4u6.webp" width="64" alt="CachyOS logo"></img>
  <br/>
  <h1 align="center">CachyOS</h1>
  <p align="center">CachyOS provides enhanced kernels that offer improved performance and other benefits.</p>
</div>


This repository contains a script for building the Linux Kernel with various optimizations from CachyOS tailored to your system's CPU architecture. The script automates the configuration and optimization of the Linux Kernel build according to your hardware and preferences and creates distributable Debian packages with these modifications.

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
2. Make the script executable with `chmod +x cachy-kernel-deb` and move the script to a directory in the `$PATH`.
3. Run the script with `cachy-kernel-deb` and follow the on-screen prompts to configure the kernel and build the packages.

# Advanced Configuration

The script includes advanced configuration options for users who want to fine-tune their kernel:

- **Linux Kernel Configuration**: Choose from different configuration profiles for the Linux Kernel from CachyOS.
- **CPU Scheduler**: Choose between schedulers like SCHED_EXT, BORE, ECHO and RT or combinations of them.
- **Configure LLVM's Link Time Optimization (LTO)**: Select from Thin and Full LTO for better optimization.
- **Configurable Tick Rate and Tick Types**: Configure the kernel tick rate and types according to your system's needs.
- **Configurable NR_CPUS**: Set the maximum number of CPUs/cores the kernel will support.
- **Configurable Hugepages**: Enable Hugepages support or not.
- **Configurable LRU**: Configure the Least Recently Used memory management mechanism.
- **Configurable Preemption Type**: Kernel preemption types generally control how the Linux kernel handles tasks and interrupts, affecting system responsiveness and latency.
    - **No Forced Preemption**: This mode disables kernel preemption entirely, only allowing preemption at explicit preemption points.
    - **Voluntary Kernel Preemption**: This mode allows the kernel to preempt tasks at certain well-defined preemption points. It offers a balance between low latency and high throughput.
    - **Preemptible Kernel (Low-Latency Desktop)**: In this mode, the kernel can be preempted almost anywhere, allowing for very low latency and high responsiveness.
    - **Real-Time Preemption**: This mode is designed for real-time applications where minimizing latency is critical.
- **Miscellanous Optimizations**: Optimizations targeting aspects of system performance and can provide benefits depending on the workload and system configuration.
    - **Use GCC -O3 Optimizations**: Aggressively optimizes compiled code for speed, possibly increasing binary size and compilation time.
    - **Enable Performance Governor**: Sets the CPU to run at maximum frequency, boosting performance but increasing power consumption and heat.
    - **Enable TCP BBR3**: A congestion control algorithm that aims to improve network throughput and reduce latency.
    - **Enable VMA Optimizations**: Enhances memory management efficiency, potentially improving application performance.
    - **Enable DAMON**: Monitors data access patterns to optimize memory usage and improve performance.
    - **Enable NUMA**: Optimizes memory allocation and access patterns on NUMA systems to reduce latency.

# Contributing

Contributions are welcome! If you have suggestions for improving the script or adding new features, please open an issue or submit a pull request.

# License

This project is licensed under the MIT License - see the LICENSE file for details.


# Issues
If you find problems with the contents of this repository please create an issue.

©2024 Nitrux Latinoamericana S.C.
