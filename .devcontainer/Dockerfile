FROM debian:testing-slim
USER root

RUN export DEBIAN_FRONTEND=noninteractive && apt-get update -y && apt-get -y upgrade --no-install-recommends && \
    apt-get install -y --no-install-recommends git curl wget command-not-found && \
    apt-get install -y --no-install-recommends build-essential gdb-multiarch clang-15 lldb-15 lld-15 clangd-15 cmake ninja-build && \
    apt-get autoremove -y && apt-get -y clean && rm -rf /var/lib/apt/lists/*

RUN echo 'root:ccyykk' | chpasswd