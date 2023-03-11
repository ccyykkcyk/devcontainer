FROM debian:testing-slim
USER root

# RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
#     && apt-get install -y --no-install-recommends build-essential cmake cppcheck valgrind clang lldb llvm gdb bash-completion command-not-found \
#     && apt-get autoremove -y && apt-get clean -y && rm -rf /var/lib/apt/lists/*

RUN export DEBIAN_FRONTEND=noninteractive && apt-get update -y && \
    apt-get install -y --no-install-recommends make dpkg-dev command-not-found && \
    apt-get install -y --no-install-recommends g++ gdb-multiarch clang clangd clang-tidy llvm lldb cmake  && \
    apt-get install -y --no-install-recommends python3 && \
    apt-get autoremove -y && apt-get -y clean && rm -rf /var/lib/apt/lists/*

RUN echo 'root:ccyykk' | chpasswd