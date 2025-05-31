FROM ubuntu:22.04

USER root
ENV USER=root

# Install package dependencies.
RUN apt-get update \
    && apt-get install -y \
    apt-utils \
    curl \
    gcc \
    && rm -rf /var/lib/apt/lists/*

# Install specific version of Rust
ENV RUST_VERSION=1.72.0
RUN curl https://sh.rustup.rs -sSf > /tmp/rustup-init.sh \
    && chmod +x /tmp/rustup-init.sh \
    && sh /tmp/rustup-init.sh -y --default-toolchain $RUST_VERSION \
    && rm -rf /tmp/rustup-init.sh

ENV PATH="$PATH:/root/.cargo/bin"
