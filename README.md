# Custom 64 bit Operating system

This is an operating system with a kernel supporting x64 bit written from scratch.

Architecture: x86 and arm64 

Bootloader: multiboot2

## Docker commands

### Building the image

Command: `docker build buildenv -t 64bit-os`

### Open the container shell

- Windows OS: `docker run --rm -it -v %cd%:/root/env 64bit-os`
- MacOS / Linux: `docker run --rm -it -v $PWD:/root/env 64bit-os`

### Make the ISO disk file

**NOTE**: Run this in the docker container following the steps above.

Command: `make build-x86_64`

### Run the OS preview using QEMU

QEMU is a virtualization tool, that helps using several stacks and test ISO files and kernels.
Get it [here](https://www.qemu.org/).

Command: `qemu-system-x86_64 -cdrom dist/x86_64/kernel.iso`
