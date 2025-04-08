FROM ubuntu:20.04

# Install necessary dependencies
RUN apt-get update && \
    apt-get install -y \
    build-essential bc bison flex libssl-dev libelf-dev wget git dkms qemu-user-static binfmt-support

# Download and install Arm GNU Toolchain
RUN wget https://developer.arm.com/-/media/Files/downloads/gnu/14.2.rel1/binrel/arm-gnu-toolchain-14.2.rel1-x86_64-aarch64-none-elf.tar.xz && \
    tar -xf arm-gnu-toolchain-14.2.rel1-x86_64-aarch64-none-elf.tar.xz -C /opt && \
    echo "export PATH=/opt/arm-gnu-toolchain-14.2.rel1-x86_64-aarch64-none-elf/bin:\$PATH" >> /root/.bashrc

# Set up environment variables
ENV PATH="/opt/arm-gnu-toolchain-14.2.rel1-x86_64-aarch64-none-elf/bin:${PATH}"
