# Support Library for SoCs from [CPUDesign-IS](https://github.com/NifleySnifley/CPUDesign-IS)

This repository contains board support, scripts, and build tools for running C programs on the RISC-V `rv32im` processor, specifically with the goal of being easy to add as a submodule to a larger project.

## Tools

- `asm2bin.py` - A wrapper for `objdump` and a utility helpful for converting `elf` executables into binary or hex files for loading into the SoC
- `ecp5progtool.py` - Bitstream reprogramming and loading tool for ECP5-based SoCs
- `create_flash_image.py` - Converts program binaries into properly formatted flash memory images for the bootloader.
- `flash_programmer.py` - Flash memory programming tool

## Build Scripts

Build scripts are provided as makefile includes in `/makefiles`

- `bootloader.defs` - Build constants for building the bootloader (minimal memory usage)
- `embedded.defs` - Build constants for building "normal" programs (libc, board support, etc.)