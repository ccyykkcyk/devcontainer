ARG VARIANT="testing"
FROM buildpack-deps:${VARIANT}-curl
USER root

RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install build-essential cmake cppcheck valgrind clang lldb llvm gdb qt6-base-dev bash-completion command-not-found \
    && apt-get autoremove -y && apt-get clean -y && rm -rf /var/lib/apt/lists/*

RUN echo 'root:ccyykk' | chpasswd

ARG USERNAME=vscode
