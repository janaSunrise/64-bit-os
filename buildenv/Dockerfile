FROM randomdude/gcc-cross-x86_64-elf

RUN apt-get -y update \
    && apt-get upgrade -y \
    && apt-get install nasm -y \
    && apt-get install xorriso -y \
    && apt-get install grub-pc-bin -y \
    && apt-get install grub-common -y \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

VOLUME /root/env
WORKDIR /root/env
