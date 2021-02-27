# Custom 64 bit Operating system

This is an operating system with a kernel supporting x64 bit written from scratch.

Architecture: x86 and arm64 
Bootloader: multiboot2

## Docker commands

### Building the image

Command: `docker build buildenv -t 64bit-os`

### Open the container shell

Windows OS: `docker run --rm -it -v %cd%:/root/env 64bit-os`
MacOS / Linux: `docker run --rm -it -v $pwd:/root/env 64bit-os`

### Run the OS preview using QEMU

Command: `qemu-system-x86_64 -cdrom dist/x86_64/kernel.iso`
